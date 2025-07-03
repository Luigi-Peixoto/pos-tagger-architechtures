# Avaliações 2 e 3 (Sala de entrega da Avaliação 2): Arquiteturas Neurais para um POS Tagger para o PTB
## OBJETIVO: Implementar 5 arquiteturas neurais (ou mais) para um POS tagger para o PTB (ver abaixo sugestões)


### AVALIAÇÃO 2: entrega quarta, 9 de julho, 23h59 (se conseguirem entregar antes, melhor)

- Entrega nesta sala do moodle: relatório descrevendo as arquiteturas neurais (ver abaixo sugestões), incluindo soluções propostas para os "issues" relevantes (ver também abaixo), resultados, e análise comparativa
 (o relatório pode ser no formato da apresentação a ser feita na semana seguinte)

Não esquecer de incluir: 

--- o link do Google Colab com a solução do problema
--- instruções de execução



### AVALIAÇÃO 3: apresentações nas aulas de segunda, 14 de julho e quarta, 16 de julho

--- o link do Google Colab com a solução do problema
--- instruções de execução

- Apresentação em aula: apresentação das alterações na arquitetura, resultados e problemas



***ALTERNATIVAS DE ARQUITETURAS NEURAIS:***
- sequence labeling tradicional, com RNNs e LSTMs uni e bidirecionais;

- uso de mais de uma camada;

- transfer learning causais usando RNNs, LSTMs (truncando o tamanho da sequencia de tags) com uma ou mais camadas

- transformers com atenção (BERT)

- transfer learners causais com entradas combinando encodings de palavras e saida do encoder

- uso de embeddings pré-treinados (frozzen ou com fine tunning) ou não



***ISSUES:***

- Compatibilização da tokenização do corpus de treino com a assumida pelos embeddings pré-treinados: don't, cousin's daughter, wanna, New York-based, ...

- Como lidou com Unknown Words. Há dois casos:

--- token não está no embedding pré-treinado e não aparece no corpus de treino

--- token não está no embedding pré-treinado mas aparece no corpus de treino

- Padding inputs

- Conciliação da classificação dos tokens com o particionamento em subwords do BERT:

--- detecção do spam na saída (acesso ao mapeamento do WordPiece)

--- determinação da tag para o token original dividido em mais de uma subwords pelo WordPiece

- outros problemas detectados
