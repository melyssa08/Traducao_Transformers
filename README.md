# Modelo de Tradução usando Transformers

Ao construir o modelo, desde a preparação dos dados até a inferência, foram observados diversos pontos, divididos em positivos e negativos:

## Pontos Positivos

- Acurácia satisfatória: O modelo alcançou uma acurácia de quase 70%. Embora não seja excelente, conseguiu traduzir sentenças de maneira que o sentido principal fosse preservado, mesmo que houvesse algumas palavras a mais ou a menos. Isso demonstra sua eficácia no contexto geral das sentenças;
- Mecanismo de autoatenção: A autoatenção permitiu capturar relações complexas entre palavras nas sentenças, facilitando a tradução e resultando em maior qualidade na correspondência entre idiomas;
- Treinamento mais rápido com paralelismo: A arquitetura dos Transformers suporta processamento paralelo, o que acelerou significativamente o treinamento, especialmente em GPUs. Isso representou uma vantagem clara em relação a modelos sequenciais como LSTM e RNN, que são naturalmente mais lentos nesse aspecto;

## Pontos Negativos

- Alta exigência computacional: O modelo Transformers demanda grande poder de processamento e memória, especialmente ao trabalhar com sequências longas. Isso requer uma infraestrutura robusta e, muitas vezes, custosa;

- Tempo de treinamento: Mesmo com GPUs avançadas, como a A100, o treinamento pode ser demorado. Por exemplo, 20 épocas podem levar cerca de 15 minutos com a A100, enquanto GPUs menos potentes podem demorar até uma hora para uma única época, evidenciando a necessidade de recursos de hardware mais avançados para tempos de execução viáveis;