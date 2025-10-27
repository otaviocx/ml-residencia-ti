# Residência em TI - TJGO
## 🧠 Projeto Final – Aplicação de Aprendizagem de Máquina em Problemas Reais

## 🎯 Objetivo Geral
Aplicar o ciclo completo de Aprendizagem de Máquina, seguindo o processo **CRISP-DM (Cross-Industry Standard Process for Data Mining)**, para desenvolver uma solução baseada em dados que responda a um problema de negócio real.

---

## 🧩 Etapas do Projeto

### **1. Entendimento do Negócio (Business Understanding)**
- Identificar um problema real com relevância prática (ex.: predição, classificação, recomendação).
- Descrever o contexto e o impacto esperado da solução.
- Formular as perguntas de negócio e definir os objetivos do projeto.
- Exemplo: *Como prever o cancelamento de clientes a partir de dados de uso?*

**Entregável:**  
📄 Documento (1 página) descrevendo o problema, o objetivo do projeto e possíveis métricas de sucesso (KPIs).

---

### **2. Entendimento dos Dados (Data Understanding)**
- Selecionar e descrever o dataset (fonte, volume, variáveis, limitações).
- Analisar a qualidade dos dados, presença de *outliers*, e distribuição das variáveis.
- Visualizar padrões iniciais e possíveis relações entre variáveis (correlação, dispersão, histogramas).

**Entregável:**  
📓 Notebook com análise exploratória (*EDA*) e breve resumo interpretativo dos achados.

---

### **3. Preparação dos Dados (Data Preparation)**
- Realizar limpeza, codificação de variáveis, normalização e engenharia de atributos.
- Criar pipeline de pré-processamento (ex.: `Pipeline` do Scikit-learn).
- Documentar as decisões tomadas e justificar as transformações realizadas.

**Entregável:**  
📓 Notebook com o pipeline completo de preparação de dados e dataset pronto para modelagem.

---

### **4. Modelagem (Modeling)**

Cada grupo deverá **escolher um tipo de aprendizado** e aplicar **duas ou mais abordagens complementares** do mesmo tipo, comparando desempenho, robustez e limitações.

---

#### 🧩 **Opção 1 – Aprendizado Supervisionado**
**Objetivo:** Prever uma variável alvo (regressão ou classificação).

**Exemplos de algoritmos:**
- Regressão Linear e Logística  
- Decision Tree, Random Forest, SVM  
- XGBoost, LightGBM  

**Frameworks recomendados:**
- [Scikit-learn](https://scikit-learn.org/stable/)  
- [XGBoost](https://xgboost.readthedocs.io/)  
- [LightGBM](https://lightgbm.readthedocs.io/)

**Métricas:**
- Regressão: MAE, RMSE, R²  
- Classificação: Accuracy, Precision, Recall, F1, ROC-AUC  

📓 *Sugestão:* comparar um modelo linear e um não linear sobre o mesmo conjunto de dados.

---

#### 🧩 **Opção 2 – Aprendizado Não Supervisionado**
**Objetivo:** Identificar padrões ou agrupar dados não rotulados.

**Exemplos de algoritmos:**
- K-Means, DBSCAN, Hierarchical Clustering  
- PCA, t-SNE (redução de dimensionalidade)

**Frameworks recomendados:**
- [Scikit-learn](https://scikit-learn.org/stable/)  
- [Yellowbrick](https://www.scikit-yb.org/en/latest/) (visualização de clusters)

**Métricas:**
- Silhouette, Calinski-Harabasz, Davies-Bouldin  

📓 *Sugestão:* comparar dois algoritmos de clusterização sobre o mesmo dataset.

---

#### 🧩 **Opção 3 – Aprendizado Semi-Supervisionado ou Auto-Supervisionado**
**Objetivo:** Usar dados parcialmente rotulados ou aprender representações sem rótulos humanos.

**Exemplos de algoritmos:**
- Label Propagation, Self-Training, Pseudo-Labeling  
- Autoencoder (para aprendizado de representações)  

**Frameworks recomendados:**
- [Scikit-learn (semi-supervised)](https://scikit-learn.org/stable/modules/label_propagation.html)  
- [TensorFlow/Keras](https://keras.io/examples/)  
- [PyTorch](https://pytorch.org/tutorials/)

📓 *Sugestão:* treinar um modelo supervisionado convencional e outro pré-treinado com autoencoder para comparação.

---

#### 🧩 **Opção 4 – Aprendizado por Reforço**
**Objetivo:** Aprender a tomar decisões por tentativa e erro, maximizando uma recompensa acumulada.

**Exemplos de algoritmos:**
- Q-Learning, SARSA (tabulares)  
- Deep Q-Network (DQN)  

**Frameworks clássicos recomendados:**
- [OpenAI Gymnasium](https://gymnasium.farama.org/) (ambientes de simulação)  
- [Stable-Baselines3](https://stable-baselines3.readthedocs.io/) (implementações simples de RL)  
- [Gymnasium Classic Control environments](https://gymnasium.farama.org/environments/classic_control/) (ex.: CartPole, MountainCar, FrozenLake)

**Métricas:**
- Recompensa média por episódio  
- Estabilidade da política aprendida  
- Taxa de sucesso  

📓 *Sugestão:* comparar Q-Learning (tabular) com DQN (rede neural simples) em um ambiente básico como CartPole.

---

#### 🧩 **Opção 5 – Sistemas de Recomendação**
**Objetivo:** Desenvolver modelos capazes de sugerir itens (produtos, filmes, cursos, etc.) a usuários com base em preferências e comportamento histórico.

**Abordagens principais:**
- **Baseadas em Conteúdo:** usam similaridade entre itens ou descrições.  
- **Colaborativas:** usam padrões de interação entre usuários e itens.  
- **Híbridas:** combinam múltiplas fontes de informação.

**Exemplos de algoritmos:**
- Filtragem Colaborativa Usuário-Usuário e Item-Item  
- Matrix Factorization (SVD, ALS)  
- Regressão para pontuação de preferência  
- Recomendação via embeddings (Word2Vec, Autoencoder)  

**Frameworks clássicos recomendados:**
- [Scikit-surprise](http://surpriselib.com/) (modelos colaborativos clássicos)  
- [Implicit](https://github.com/benfred/implicit) (ALS e recomendações implícitas)  
- [TensorFlow Recommenders](https://www.tensorflow.org/recommenders)  
- [LightFM](https://making.lyst.com/lightfm/docs/home.html) (modelo híbrido simples e eficiente)

**Métricas:**
- Precision@K, Recall@K  
- Mean Average Precision (MAP)  
- Normalized Discounted Cumulative Gain (nDCG)  

📓 *Sugestão:* implementar e comparar duas abordagens distintas — por exemplo, um modelo de filtragem colaborativa e outro baseado em conteúdo — e avaliar o desempenho com métricas de ranking.

---

**Entregável (para todas as opções):**  
📓 Notebook com experimentos e comparação crítica entre as abordagens do mesmo tipo de aprendizado, destacando vantagens, limitações e aplicabilidade prática.

---

### **5. Avaliação (Evaluation)**
- Avaliar os modelos com métricas adequadas:
  - **Regressão:** MAE, RMSE, R²  
  - **Classificação:** Precision, Recall, F1-score, ROC-AUC  
  - **Clusterização:** Silhouette, Calinski-Harabasz  
- Comparar o desempenho entre modelos e discutir a adequação de cada um ao problema de negócio.
- Relacionar as métricas de ML com indicadores reais (KPIs).

**Entregável:**  
📄 Relatório técnico (2–3 páginas) contendo as métricas, gráficos e análise crítica dos resultados.

---

### **6. Implantação e Comunicação (Deployment)**
- Preparar uma **apresentação de 5 a 8 minutos** contendo:
  - Problema → Solução proposta → Resultados → Conclusões.
- Entregar notebook final e slides com visualizações e conclusões.
- (Opcional) Expor o modelo via API simples (Flask/FastAPI) ou dashboard (Streamlit).

**Entregável:**  
🎤 Apresentação final + link para o repositório (GitHub, Google Colab, ou Kaggle Notebook).

---

## 📊 Critérios de Avaliação

| Critério | Peso | Descrição |
|-----------|------|-----------|
| **Entendimento do negócio** | 15% | Clareza e relevância da formulação do problema. |
| **Entendimento e análise dos dados** | 15% | Qualidade da análise exploratória e insights obtidos. |
| **Preparação dos dados** | 20% | Correção e justificativa das transformações. |
| **Modelagem** | 30% | Aplicação e comparação de algoritmos. |
| **Avaliação e interpretação** | 20% | Uso correto de métricas e análise crítica. |

---

## 💼 Ideias de Projetos para o TJ

A seguir estão sugestões de temas e linhas de investigação que os grupos podem explorar no projeto final, considerando o contexto do Tribunal de Justiça.

---

### 🧩 **1. Aprendizado Supervisionado**
Foco em **previsão e classificação** com dados rotulados.

- Previsão do **tempo médio de tramitação** de processos com base em tipo, assunto e histórico.  
- Classificação automática de **tipos de petições** (inicial, recurso, manifestação, despacho).  
- Identificação de **processos com alto risco de atraso**.  
- Predição de **reforma de sentença** em instâncias superiores.  
- Classificação de **decisões judiciais** (deferimento, indeferimento, arquivamento).

---

### 🧩 **2. Aprendizado Não Supervisionado**
Foco em **descoberta de padrões e agrupamentos** sem rótulos.

- Agrupar **decisões ou acórdãos** por similaridade de conteúdo jurídico.  
- Clusterizar **processos semelhantes** em estrutura ou tramitação.  
- Detectar **anormalidades** em prazos ou movimentações processuais.  
- Descobrir **perfis de produtividade** de varas, juízes ou servidores.  
- Identificar **padrões incomuns** em dados administrativos ou financeiros.

---

### 🧩 **3. Aprendizado Semi-Supervisionado e Auto-Supervisionado**
Foco em **aproveitar grandes volumes de dados com poucos rótulos**.

- Classificar **tipos de decisões** com apenas um pequeno conjunto de exemplos rotulados.  
- Criar **embeddings de textos jurídicos** com autoencoders para melhorar outras tarefas de ML.  
- Detectar **sentenças atípicas** ou **decisões fora do padrão** em grandes bases de acórdãos.  
- Usar *pseudo-labeling* para expandir conjuntos de dados de petições parcialmente rotuladas.

---

### 🧩 **4. Aprendizado por Reforço**
Foco em **otimizar políticas e fluxos de decisão sequencial**.

- Simular **distribuição de processos entre servidores ou varas**, buscando equilibrar carga de trabalho.  
- Aprender políticas de **priorização de tarefas** (por tipo de processo, prazos ou impacto).  
- Otimizar o **uso de recursos computacionais** em filas de processamento automatizado.  
- Modelar um agente que aprenda a **minimizar atrasos** em trâmites administrativos ou judiciais.

*(Esses projetos podem usar simulações simples com `Gymnasium` e `Stable-Baselines3`, representando o fluxo de processos como um ambiente interativo.)*

---

### 🧩 **5. Sistemas de Recomendação**
Foco em **apoio à decisão e recuperação inteligente de informação jurídica**.

- Recomendação de **jurisprudências semelhantes** para casos em análise.  
- Sugestão de **artigos de lei ou dispositivos legais** relevantes para um texto de petição.  
- Recomendação de **modelos de documentos** (despachos, decisões) com base em casos anteriores.  
- Sugestão de **tarefas prioritárias** ou **distribuição otimizada de processos** a servidores.  
- Recomendação de **cursos e materiais de capacitação** a magistrados e servidores conforme perfil e histórico de atuação.

*(Esses projetos podem usar bibliotecas como `Scikit-surprise`, `LightFM`, `Implicit` ou `TensorFlow Recommenders`.)*

---

## 🧠 Ferramentas Recomendadas
- **Linguagem:** Python  
- **Bibliotecas:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, TensorFlow/Keras  
- **Ambiente:** Google Colab ou Jupyter Notebook  
- **Versionamento:** GitHub  
- **Fontes de Dados:** TJGO, Kaggle, Open Data Brasil, etc.

---

## 📅 Entregas Sugeridas

| Etapa | Entregável | Prazo sugerido |
|-------|-------------|----------------|
| Entendimento do negócio e dos dados | Documento + EDA | Semana 6 |
| Preparação e modelagem inicial | Pipeline + Experimentos iniciais | Semana 7 |
| Avaliação e refinamento | Relatório técnico | Semana 8 |
| Apresentação final | Slides + Repositório | Semana 9 |

---

## 📘 Referências
- LESKOVEC, J.; RAJARAMAN, A.; ULLMAN, J. *Mining of Massive Datasets*. Cambridge University Press, 2020.  
- GERON, A. *Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow*. O’Reilly, 2022.  
- ZHOU, Z.-H. *A Brief Introduction to Weakly Supervised Learning*. *National Science Review*, 2021.  
- VAN ENGENLEN, T.; HOOS, H. *A Survey on Semi-Supervised Learning*. *Machine Learning Journal*, Springer, 2020.  
- RICCI, F.; ROKACH, L.; SHAPIRA, B. *Recommender Systems Handbook*. Springer, 2022.

---

✳️ **Entrega Final:**  
Os alunos deverão submeter:
1. **Notebook completo** (com todas as etapas do CRISP-DM).  
2. **Relatório técnico (PDF)**.  
3. **Apresentação (slides)**.  
4. **Link para o repositório** contendo código e documentação.
