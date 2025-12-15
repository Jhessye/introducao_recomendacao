# Sistema de Recomendação – Primeiros Passos

Exploração de heurísticas simples de recomendação utilizando **Pandas**, análise de similaridade entre usuários e construção das primeiras ideias para um motor de recomendação filmes, usando a ideia básica de KNN.

---

## Projeto

Este repositório contém um notebook introdutório onde exploro diferentes abordagens para criar um sistema de recomendação, indo do mais simples (baseado em contagem de votos) ao mais elaborado (similaridade entre usuários).
O objetivo é entender a lógica por trás de modelos de recomendação antes de avançar para técnicas mais complexas como filtragem colaborativa ou modelos baseados em machine learning usando KNN.

---

## Notebook

###  1. Heurística baseada no total de votos

Primeira abordagem utilizando apenas **Pandas**:

* Filmes/itens mais votados tendem a ser mais relevantes.
* Simples, rápida e uma ótima linha de base (baseline).

###  2. Nova heurística: Nota média + filtro de quantidade mínima de votos

Melhoria da heurística anterior:

* Considera a **qualidade** (média das avaliações);
* Evita recomendações com poucos votos, aplicando um “filtro de confiança”.

###  3. Procura por usuários "similares"

Introdução ao conceito de filtragem colaborativa:

* Para cada par de usuários, calcular a **distância entre notas**.
* Quanto menor a diferença absoluta das avaliações, maior a similaridade.
* Exemplo:

  * João deu nota 4 ao filme A
  * Maria deu nota 1 ao mesmo filme
  * Distância = |4 - 1| = 3

###  4. Cálculo da distância entre usuários

* Utilização de métricas baseadas em diferenças de notas;
* Étapa fundamental para prever gostos de um usuário a partir de outros com perfil semelhante.

---

## Tecnologias

* **Python 3.x**
* **Pandas**
* **Google Colab** (badge incluído no notebook original)

---

## Como Executar

1. Clone o repositório:

   ```bash
   git clone https://github.com/SEU-USUARIO/SEU-REPO.git
   ```
2. Abra o notebook no Jupyter Notebook ou Google Colab.
3. Instale as dependências (se necessário):

   ```bash
   pip install pandas
   ```

---

## Objetivo

Este projeto foi criado com foco em **aprendizado prático** de sistemas de recomendação, servindo como base para:

* Filtragem colaborativa baseada em usuários
* Filtragem colaborativa baseada em itens
* Modelos baseados em machine learning
* Algoritmos como SVD, KNN, etc.

---

## Licença

Este projeto é open-source — fique à vontade para estudar, modificar e evoluir!
