# Challenge_-DS_Alura_TelecomX_BR
Desafio para exercitar o aprendizado em ETL no curso de Data Science

# 📊 Análise de Evasão de Clientes (Churn) da TelecomX_BR

Este projeto faz parte do programa ONE (Oracle Next Education) G8 BR Data Science, parceria entre a Alura e a Oracle, e tem como objetivo analisar o comportamento dos clientes de uma empresa de telecomunicações, buscando entender os fatores que influenciam o cancelamento de serviços (Churn). Através de análise estatística, visualização de dados e interpretação de padrões, propomos insights e recomendações para mitigar a evasão de clientes.

---

## 🎯 Objetivo


A extração dos dados da empresa estão em uma API que está armazenada dentro de um repositório no GitHub.

A transformação, tratamento e limpeza desses dados.

Em seguida analisar esse dados, para investigar os principais fatores que contribuem para a evasão de clientes, utilizando dados históricos da base de clientes. A análise busca responder às seguintes perguntas:

- Qual o perfil dos clientes que mais cancelam?
- Quais características estão mais associadas ao churn?
- Como podemos prever e prevenir futuros cancelamentos?

---

## 📁 Estrutura do Repositório

O repositório está organizado da seguinte forma:

```
📦Challenge_TelecomX_BR/
 ┣ 📊 challenge_TelecomX_BR.ipynb
 ┣ 📈 histograma.png
 ┣ 📈 proporcao-evasao-clientesa.png
 ┣ 📑 README.md
```

- `Challenge_TelecomX_BR.ipynb`: notebook com todo o processo de análise.
- `histograma.png`: Distribuição das variáveis numéricas com relação a Churn.
- `proporcao-evasao-clientesa.png`: **Gráfico de Barras**: mostra a contagem absoluta de clientes que saíram (`1`) e que permaneceram (`0`).
 **Gráfico de Pizza**: mostra a proporção percentual entre os dois grupos.
- `README.md`: este documento.


---

## 🛠️ Tecnologias Utilizadas

* **Python** (versão 3.x)
* **Bibliotecas Python:**
    * `pandas` para manipulação e análise de dados.
    * `numpy` para operações numéricas.
    * `matplotlib` para visualização de dados estática.
    * `seaborn` para visualizações estatísticas atraentes.
* **Ambiente de Desenvolvimento:** Google Colab (ou Jupyter Notebook).

---

## ⚙️ Instalação e Configuração

Para executar este projeto localmente (em Jupyter Notebook) ou reproduzi-lo no Google Colab, siga os passos abaixo:

1.  **Clonar o Repositório:**
    ```bash
    git clone [https://github.com/Eduardo-Marchi2025/Challenge_-DS_Alura_TelecomX_BR.git)
    cd Desafio_DataX
    ```

2.  **Criar Ambiente Virtual (Recomendado - para uso local):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # No Windows: .\venv\Scripts\activate
    ```

3.  **Instalar Dependências:**
    ```bash
    pip install pandas numpy matplotlib seaborn
    ```

---

## 🚀 Como Executar a Análise

### No Google Colab:

1.  **Upload do Arquivo:** Faça o upload do arquivo `TelecomX_Data.json` para o ambiente do Google Colab (na sessão de arquivos, clique no ícone de "Upload"). Certifique-se de que ele esteja na pasta `/content/`.
2.  **Abrir o Notebook:** Abra o arquivo `Challenge_TelecomX_BR/.ipynb` no Google Colab.
3.  **Executar as Células:** Execute todas as células do notebook sequencialmente. O notebook está estruturado para realizar o pré-processamento, as análises e gerar os gráficos e o relatório final.

### No Jupyter Notebook (Localmente):

1.  **Certifique-se de que os arquivos `Challenge_TelecomX_BR/.ipynb` e `TelecomX_Data.json` estão no mesmo diretório.**
2.  **Abrir Jupyter:** Inicie o Jupyter Notebook ou JupyterLab a partir do terminal no diretório do projeto:
    ```bash
    jupyter notebook
    ```
3.  **Abrir o Notebook:** No navegador, clique em `Desafio Data_X.ipynb` para abri-lo.
4.  **Executar as Células:** Execute todas as células do notebook em ordem para reproduzir a análise completa.

---

## 🔬 Transformação, tratamento e limpeza de Dados

* ⚖️ **Normalização de colunas aninhadas**

* 💱 **Transformar os dados da coluna `total_charges` de strings para "float64" (Decimais).**

* 🗑️ **Remoção de registros com valores ausentes ou nulos**

* ⚖️ **Padronização da mesma informação com "texto" diferente.**

* 💱 **Conversão de variáveis binárias** de `"Yes"/"No"` para `1/0`.

* 🌏 **Padronização de nomes de colunas** para o formato `Snake_case` (ex: `charges_total`).

* 🧮 **Criação da variável derivada `dayle_charge`**, com base no gasto mensal.

---

## 📊 Análise Exploratória

A análise utilizou gráficos de barras e setores, histogramas e boxplots para examinar:

- Diferenças entre clientes com e sem churn
- Padrões em variáveis como:
  - Tempo de contrato
  - Valores mensais
  - Valores totais
  - Valores diários

**Histogramas e Boxplots:** ![Histograma]![Image](https://github.com/user-attachments/assets/7f3b7fb4-6df5-44f5-a83f-23230473ac16)

---

## 📊 Visualização da Evasão de Clientes (Churn)

A seguir, apresentamos dois gráficos que ilustram a distribuição da variável `churn`, responsável por indicar se o cliente deixou ou permaneceu na empresa:

- **Gráfico de Barras**: mostra a contagem absoluta de clientes que saíram (`1`) e que permaneceram (`0`).
- **Gráfico de Pizza**: mostra a proporção percentual entre os dois grupos.

| Distribuição Absoluta e Percentual |
|-----------------------|
| ![Gráfico]![Image](https://github.com/user-attachments/assets/ea813bc5-ab6e-4af5-95f1-61283f43a0a3) |

> 📌 Os gráficos acima revelam que cerca de **26,6% dos clientes saíram da empresa**, enquanto **73,4% permaneceram**.

## 📣 Conclusões e Inferências

* A análise do churn revela padrões importantes sobre os clientes que cancelam seus serviços. Observamos que a evasão é predominantemente registrada entre usuários que possuem pouco tempo de contrato com a empresa.

* Há também, os clientes com contratos mensais apresentam os maiores índices de churn, sugerindo uma maior vulnerabilidade desse modelo de assinatura. A cobrança via electronic check também se destaca como um fator associado ao cancelamento, possivelmente devido à pouca praticidade desse método de pagamento.

* Clientes que pagam mais por mês e não utilizam serviços adicionais estão mais propensos a cancelar, reforçando a importância de agregar valor à experiência do cliente.

* Clientes mais antigos tendem a ser mais fiéis, apontando para a importância do onboarding e fidelização inicial.

* Pacotes com múltiplos serviços demonstram retenção mais eficaz.


## 🏹 Recomendações

Com base nas estatítiscas medidas e nas inferências das observações, recomenda-se que a Telecom X adote estratégias para minimizar a evasão e fortalecer a retenção de clientes:
1. **Incentivar contratos de longo prazo:** Criar programas de fidelidade, oferecer descontos progressivos ou benefícios exclusivos para clientes que optam por assinaturas anuais.

2. **Ampliar o valor dos serviços adicionais:** Estimular a adesão a pacotes como suporte técnico premium, segurança online ou benefícios exclusivos para quem utiliza mais serviços da empresa.

3. **Revisar métodos de pagamento:** Reduzir a dependência do electronic check, promovendo opções mais convenientes como débito automático, cartão de crédito ou PIX, para facilitar transações e reduzir cancelamentos.

4. **Aprimorar o suporte nos primeiros meses:** Implementar uma jornada de boas-vindas personalizada, com contato proativo, ofertas especiais e suporte dedicado para os novos clientes.

5. **Oferecer pacotes com múltiplos serviços essenciais com desconto** (ex: suporte técnico + backup).

6. **Incentivar contratos de longo prazo** com benefícios claros para reduzir evasão mensal.

7. **Monitorar novos clientes** nos primeiros meses com campanhas de retenção e atendimento proativo.

7. **Avaliar descontos em planos com fatura muito elevada**, pois estão associados a maiores taxas de churn.

8. **Estudar os perfis com churn elevado para campanhas personalizadas de reengajamento**.

9. Estudo detalhado das informações da "entrevista" do cancelamento do contrato.
---

🎯 Próximos Passos
Preparar os dados para uma modelagem preditiva.

Aplicar técnicas de balanceamento de classe (SMOTE, undersampling) para corrigir o desbalanceamento da variável Churn.

Treinar e avaliar modelos preditivos com foco em interpretabilidade e ações práticas.
---

## ✒️ Autor ✒️

Projeto desenvolvido por **Eduardo Marchi** como parte do Challenge da Trilha de Especialização em Data Science do Programa ONE G8: Oracle Next Education em parceria com a Alura:

**Eduardo Marchi**

* 📎 GitHub: [![GitHub followers](https://img.shields.io/github/followers/Eduardo-Marchi2025?style=social)](https://github.com/Eduardo-Marchi2025)
* <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linkedin/linkedin-original.svg" width="20" height="20">: https://www.linkedin.com/in/eduardo-marchi-42b371348/
* 📧 e-mail: eduardo.marchi@gmail.com

---

## 📝 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).


