# 🚗 Previsão de Preços de Carros Usados com Machine Learning

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-black?style=for-the-badge&logo=flask&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=for-the-badge&logo=render&logoColor=white)

Projeto final desenvolvido para o curso de **Fundamentos de Inteligência Artificial e Análise de Dados** no SENAI. 

## 📋 Sobre o Projeto

Este projeto consiste em uma solução de ponta a ponta (End-to-End) de Machine Learning para estimar o valor de mercado de veículos usados. A partir de uma base de dados histórica (`dataset_carros_usados.csv`), o modelo de **Regressão Linear** analisa padrões e correlações para realizar previsões de preços via uma API REST desenvolvida em Flask, que é consumida por uma interface web interativa.

## 🔗 Links do Projeto (Em Produção)

| Plataforma | Link de Acesso | Descrição |
| :--- | :--- | :--- |
| 🌐 **Site / FrontEnd** | [Wheel Price Predictor](https://wheel-price-predictor.lovable.app/) | Interface web interativa para realizar previsões de forma intuitiva. |
| 🚀 **API REST / BackEnd** | [API no Render](https://projeto-final-analise-dados-tarde.onrender.com/) | Servidor na nuvem hospedando o modelo de Machine Learning. |

## 🛠️ Tecnologias Utilizadas

**🐍 Linguagem & Machine Learning**
*   **Python 3:** Linguagem principal do projeto.
*   **Pandas & NumPy:** Manipulação, tratamento e análise exploratória de dados.
*   **Scikit-Learn:** Construção, treinamento e avaliação do modelo de machine learning.
*   **Seaborn/Matplotlib:** Visualização de dados e geração de gráficos estatísticos (EDA).

**🌐 BackEnd & API**
*   **Flask:** Framework micro-web utilizado para estruturar os endpoints da API.
*   **Flask-CORS:** Habilitação de requisições de diferentes domínios.

**☁️ Deploy, CD & FrontEnd**
*   **Render:** Hospedagem em nuvem da API REST.
*   **Lovable:** Desenvolvimento e hospedagem da interface Web (FrontEnd).

## ⚙️ Variáveis do Modelo (Features)

Para estimar o valor de um veículo, o modelo leva em consideração 4 variáveis principais:
1. **Ano de fabricação:** Ano do modelo/fabricação do veículo.
2. **Quilometragem:** Distância total percorrida (em km).
3. **Motor:** Potência ou cilindrada do motor (ex: 1.0, 1.6, 2.0).
4. **Quantidade de revisões:** Número de revisões periódicas realizadas no histórico do veículo.

## 📊 Metodologia e Principais Insights

Durante o desenvolvimento deste projeto, foram realizadas as seguintes etapas:
1. **Análise Exploratória de Dados (EDA):** Entendimento da base de dados, identificação de possíveis outliers e análise de correlação entre as variáveis e o preço do veículo.
2. **Treinamento do Modelo:** Escolha do algoritmo de Regressão Linear, divisão dos dados em treino e teste (Train-Test Split) e ajuste matemático do modelo.
3. **Desenvolvimento da API:** Criação das rotas GET (para verificação de status) e POST (para recebimento dos dados via JSON e retorno da previsão) utilizando Flask.
4. **Deploy:** Hospedagem da API na nuvem (Render) e criação da interface de usuário (Lovable).

**🔍 Descobertas da Análise Exploratória:**
Ao analisar as correlações para a construção do modelo preditivo, destacam-se os seguintes comportamentos nos dados:
* **Fator de Valorização (Ano e Motor):** O ano de fabricação possui a correlação positiva mais forte com a variável alvo (preço), definindo o valor base do carro. A potência do motor também atua como um multiplicador de valor.
* **Fator de Depreciação (Quilometragem):** A quilometragem atua como o principal ofensor do preço. O modelo identificou uma clara correlação negativa: veículos com alta quilometragem sofrem penalizações significativas no valor estimado, independentemente do ano.
* **Retenção de Valor (Revisões):** A quantidade de revisões impacta positivamente na retenção do preço do veículo, indicando matematicamente que o mercado valoriza históricos de manutenção comprovada.

## 🚀 Como Utilizar (How to Use)

Você pode testar e utilizar o projeto de três formas diferentes:

### 1️⃣ Opção A: Utilizando a Interface Web (Mais Rápido)
1. Acesse o site oficial: [Wheel Price Predictor](https://wheel-price-predictor.lovable.app/).
2. Preencha os campos com os dados do veículo.
3. Clique no botão de cálculo para visualizar a estimativa.

### 2️⃣ Opção B: Consumindo a API REST (Em Nuvem)
Para verificar se a API está online (GET):
```bash
curl -X GET [https://projeto-final-analise-dados-tarde.onrender.com/](https://projeto-final-analise-dados-tarde.onrender.com/)

```

Para fazer uma previsão enviando um JSON (POST):

```bash
curl -X POST [https://projeto-final-analise-dados-tarde.onrender.com/prever](https://projeto-final-analise-dados-tarde.onrender.com/prever) \
-H "Content-Type: application/json" \
-d '{"ano": 2018, "quilometragem": 50000, "motor": 1.6, "num_revisoes": 5}'

```

### 3️⃣ Opção C: Executando Localmente

Se quiser rodar o projeto na sua própria máquina, siga os passos:

1. Clone o repositório:

```bash
git clone [https://github.com/lmTinelli/Projeto-Final-Senai.git](https://github.com/lmTinelli/Projeto-Final-Senai.git)
cd Projeto-Final-Senai

```

2. Instale as dependências necessárias:

```bash
pip install -r requirements.txt

```

3. Execute a API:

```bash
python app.py

```

A API estará rodando em `http://localhost:8000`.

---

*Projeto baseado nas orientações do [Repositório do Professor Platini](https://github.com/ProfPlatini/PROJETO-FINAL-ANALISE-DADOS-TARDE).*

## 📬 Contato

Desenvolvido por **Luiz Marcelo Tinelli** 

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/luiz-marcelo-tinelli-14491b229/)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:luizmarcelotinelli@gmail.com)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/5519994198900)
