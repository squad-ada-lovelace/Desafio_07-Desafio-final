# 🗓️ Calendário

##  30/09 (quarta)
- Verificar tipos de dados, distribuição das variáveis e presença de nulos (df.info(), df.describe(), df.isnull().sum()).
- Mapear a variável alvo: O dataset original traz a coluna de qualidade do sono (Quality of Sleep [1-10]) ou o distúrbio de sono (Sleep Disorder). De acordo com as instruções do desafio:
    - Criar a classe categorizada para a **Qualidade do Sono: Ruim (0-4), Moderada (5-6) e Boa (7-10)**.
- Gerar uma matriz de correlação simples e alguns boxplots rápidos (ex: Estresse vs Qualidade do Sono, Idade vs Qualidade do Sono) para responder às perguntas de Análise Exploratória do item 1.

Observações do dia:
- Squad
    - Definiu-se que vamos fazer sessões síncronas a partir de segunda (05/10)

- Processamento e análise exploratória
    - Rodando um df.corr() nas variáveis numéricas, aparentemente há uma correlação negativa bem forte entre **qualidade do sono** e **estresse** (-0,9). Levemente negativa entre **qualidade do sono** e **batimentos cardíacos** (-0,66) e fortemente positiva entre **qualidade do sono** e **duração do sono** (0,88)
    - Rodei o pairplot pra procurar correlações a serem investigadas. As que mais parecem merecer atenção são:
        - Qualidade do sono e idade
        - Qualidade do sono e tempo diário de atividade física
        - Qualidade do sono e nível de estresse
        - Qualidade do sono e duração do sono
        - Tempo de atividade física e duração do sono
        - Nível de estresse e duração do sono
        - Passos diários e duração do sono
        - Passos diários e pressão
    - Fiz a tabela de contingência para avaliar a distribuição de variáveis categóricas e a princípio, sem maiores investigações:
        - Homens dormem pior que mulheres
        - Engenheiros de software, representantes de venda e vendedores dormem pior
        - Quem está no IMC de obesidade dorme pior


- Questões
    - Como dividir a idade em faixas? É preciso? Algumas saídas podem ser talvez ver como a idade reage a correlação.
    - Percebo que provavelmente vamos precisar de um campo para pressão baixa, normal e alta.
    - No geral, a tabela de contingência me faz questionar a qualidade do estudo e a proveniência dos dados. Desconfio que a amostragem é bem ruim, apenas 374 pessoas. Talvez seja representativo se se tratar de uma empresa.

## 03/10 (sábado)

## 04/10 (domingo)

## Checklist

- Análise Exploratória:
- [x] Primeira versão processada do dataset
- [x] Distribuição visual das variáveis. 
- [x] Principais correlações com a Qualidade do Sono.
- [x] Diferenças registradas por Gênero e Faixa Etária. 

- Pré-processamento:
- [ ] Tratamento de nulos
- [ ] Encoding de categóricas e escala de numéricas.

- Modelagem & Avaliação:
- [ ] Pelo menos 1 modelo treinado e avaliado (Acurácia, Precision, Recall, Matriz de Confusão).
- [ ] Resposta justificada sobre a melhor métrica para o problema.
- Interpretação & Recomendação:
- [ ] Identificação dos fatores com maior impacto (positivo e negativo).
- [ ] Recomendações de ação para a empresa de saúde digital. 