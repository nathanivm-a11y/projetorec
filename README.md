# Projeto de Previsão de Cancelamento de Clientes (Churn)

## Sobre o Projeto
Fala pessoal! Esse é o meu projeto de recuperação do módulo de Inteligência Artificial. O objetivo aqui foi pegar uma base histórica de clientes de uma operadora de telecomunicações e criar um modelo preditivo para descobrir quem tem mais chance de cancelar o contrato.

## O Problema que Resolvemos
A lógica é simples: perder cliente custa caro para a empresa. Se a gente conseguir usar inteligência artificial para prever quais clientes estão insatisfeitos e prestes a sair, a equipe de marketing consegue agir antes. Dá para oferecer um desconto ou um suporte melhor e salvar o contrato antes que o cancelamento de fato aconteça.

## Técnicas e Tecnologias Utilizadas
Eu fiz tudo em Python, usando o formato de Jupyter Notebook. As principais bibliotecas que usei foram Pandas, Numpy, Matplotlib, Seaborn e o Scikit-Learn para a parte de Machine Learning.

O projeto foi dividido nestas fases principais:
* Análise Exploratória (EDA): Olhei os dados e vi que a base era bem desbalanceada e que algumas colunas tinham muita correlação.
* Limpeza de Dados: Tirei as duplicatas e preenchi os dados em branco (nulos) usando a mediana, pra evitar que os outliers distorcessem tudo.
* Feature Engineering: Criei uma coluna nova de gasto médio mensal pra ajudar o modelo a achar padrões.
* Balanceamento: Tinha muita gente que não cancelava na base. Fiz um under sampling para igualar o jogo, mas apliquei isso só nos dados de treino para o modelo não "colar" na hora do teste final.
* Escalonamento: Usei o StandardScaler só para os dados do KNN, porque ele é sensível ao tamanho dos números.
* Modelos Avaliados: Testei o KNN e a Árvore de Decisão, ajustando os parâmetros deles para evitar o overfitting (quando o modelo só decora os dados de treino).

## Veredito Final
Depois de treinar e testar tudo em uma parcela de dados que os modelos nunca tinham visto (os 20% de teste), a Árvore de Decisão foi a vencedora. Ela chegou a uma acurácia de aproximadamente 73.7%. 

Eu recomendo a Árvore para a empresa porque, diferente de outros modelos que são uma "caixa preta", ela é explicável. Dá para mostrar para a equipe de marketing exatamente quais regrinhas (como tempo de contrato) fizeram o modelo achar que aquele cliente ia cancelar.

## Como Executar o Sistema
Se você quiser rodar esse código na sua máquina, é só seguir esses passos:

1. Faça o clone deste repositório.
2. Instale as bibliotecas necessárias. Tem um arquivo chamado requirements.txt com a lista, é só rodar: pip install -r requirements.txt
3. Garanta que o arquivo dataset_recuperacao_telecom.csv está guardado dentro de uma pasta chamada data/ na mesma raiz do projeto.
4. Abra o arquivo Projeto_Final_Telecom.ipynb e rode as células de código uma por uma.

## Melhorias Futuras
Se a gente fosse dar continuidade nesse projeto, eu sugeriria algumas melhorias:
1. Testar algoritmos mais complexos e potentes, como o Random Forest.
2. Criar uma API para que o sistema da empresa pudesse consultar o risco de um cliente em tempo real.

---
Apresentação em Vídeo:

