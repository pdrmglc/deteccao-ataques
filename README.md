# Detecção de Ataques DDoS em Dados de Tráfego de Rede
## Problema

Nosso cliente enfrentou um ataque de negação de serviço distribuído (DDoS), caracterizado por uma elevação repentina no tráfego de requisições HTTP. O desafio é detectar esses ataques o mais rápido possível, distinguindo entre o tráfego malicioso e o tráfego legítimo da aplicação, a fim de mitigar o impacto do ataque sem afetar a experiência do usuário.

## Contexto
Os conjuntos de dados fornecidos consistem em registros de tráfego de rede, capturados em dois períodos distintos: um período de tráfego normal e um período que inclui um ataque DDoS. A análise exploratória desses dados é essencial para identificar padrões e características que possam indicar a ocorrência de um ataque.

## Metodologia

### Preparação do ambiente de trabalho

1. Criação de um ambiente py-env para isolar dependências
2. Uso do Jupyter-lab para organização do fluxo de trabalho
3. Criação de repositório remoto no GitHub para documentação do protocolo

### Análise Exploratória de Dados:

1. Identificação de estatísticas descritivas e características relevantes dos dados.
2. Exploração dos atributos dos conjuntos de dados arquivo_sem_ataque.csv e arquivo_com_ataque.csv para entender suas diferenças.
3. Utilização da derivada da curva de tráfego para identificar mudanças súbitas na angulação, indicando possíveis ataques DDoS. Testes de hipóteses simples podem ser realizados para calcular a probabilidade de ocorrência dessas mudanças.

### Detecção de Anomalias e Ataques:

1. Utilização de métricas como número de requisições por intervalo de tempo para identificar padrões anômalos.
2. Comparação entre o tráfego normal e o tráfego durante o ataque para identificar aumentos repentinos no volume de requisições.


### Modelagem de Classificação:

1. Desenvolvimento de um modelo de aprendizado de máquina para diferenciar entre requisições de tráfego legítimo e requisições de tráfego malicioso.
2. Utilização de técnicas de clusterização para identificar grupos de padrões de tráfego suspeitos, mesmo sem informações prévias sobre os atacantes.

### Premissas e Escolhas

1. Seleção de Atributos Relevantes: A escolha dos atributos para análise e modelagem é baseada na sua relevância potencial para distinguir entre tráfego normal e tráfego malicioso.
2. Detecção de Anomalias: A detecção de ataques é baseada na identificação de padrões anômalos no tráfego de rede, como aumentos repentinos no volume de requisições.
3. Modelagem Supervisionada e Não Supervisionada: Optou-se por uma abordagem híbrida, combinando técnicas de aprendizado supervisionado e não supervisionado para desenvolver um modelo robusto de detecção de ataques DDoS.

Esta metodologia visa fornecer uma abordagem sistemática e fundamentada para detecção e diferenciação de ataques DDoS em dados de tráfego de rede, permitindo uma resposta rápida e eficaz para mitigar os impactos dos ataques à segurança da aplicação.