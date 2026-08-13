# Miniguia de Estudos: Matemática Financeira para Concurso Banco do Brasil

## 1. Contexto e Objetivos

Estou me preparando para o concurso do Banco do Brasil (escriturário/agente comercial) e escolhi Matemática Financeira como tema deste caderno por ser uma das áreas onde sinto mais dificuldade, especialmente em:
- Juros simples e compostos
- Equivalência de taxas
- Sistemas de amortização (SAC/PRICE)
- Cálculos de porcentagem

**Objetivo**: Usar o NotebookLM como ferramenta de estudo ativo para consolidar esses conceitos, criar um material de revisão confiável e testar como a IA pode apoiar 
(e onde falha) no aprendizado desse conteúdo.

## 2. Curadoria de Fontes

Para este caderno temático, selecionei 4 fontes abertas, priorizando material específico para o concurso do Banco do Brasil e para a banca CESGRANRIO:

1. **Prova Comentada - Banco do Brasil 2021 (Escriturário Agente Comercial)**  
   Prova real aplicada pelo BB em 2021, com gabarito comentado.  
   [Link](https://mkt.estrategia.com/concursos/wp-content/uploads/sites/2/2024/12/Banco-do-Brasil-2021-Escriturario-Agente-Comercial-Prova-Comentada-LP.pdf)

2. **Matemática Financeira CESGRANRIO - Questões Comentadas (Prof. Daniela Arboite)**  
   Coletânea de questões comentadas de matemática financeira cobradas pela banca CESGRANRIO em concursos bancários (BB, Banrisul, BASA, CEF).  
   [Link](https://api.pageplace.de/preview/DT0400.3410006668659_A50641367/preview-3410006668659_A50641367.pdf)

3. **Apostila Opção - Banco do Brasil Agente Comercial**  
   Apostila preparatória específica para o cargo de Agente Comercial do BB.  
   [Link](https://www.apostilasopcao.com.br/arquivos-opcao/apostilas/18405/91413/op-118dz-22-banco-brasil-agt-com.pdf)

4. **Vídeo: "Concurso Banco do Brasil 2026 | Matemática Financeira: Conceitos Gerais"**  
   Aula em vídeo (canal Nova Concursos) cobrindo juros simples, juros compostos, capital/taxa/tempo, montante, desconto simples, taxa nominal e efetiva, e sistemas de capitalização — com foco nos erros mais comuns dos candidatos.  
   [Link](https://www.youtube.com/live/l1kpqh5BF-4)

## 3. Engenharia de Prompts e Troubleshooting

### Prompt 1: "Explique o conceito de juros compostos com um exemplo prático de concurso bancário"

**Resposta obtida (resumo):**
A IA explicou o conceito de juros compostos ("juros sobre juros"), apresentou a fórmula M = C.(1+i)^n, e trouxe um exemplo real de prova (Casa da Moeda, 2024): um investimento de R$ 20.000,00 a 1% ao mês por 3 meses, mostrando o cálculo mês a mês até chegar em R$ 20.606,02, comparando com o resultado do regime de juros simples (R$ 20.600,00) para destacar a diferença entre os dois regimes.

**O que funcionou bem:**
- Trouxe a fórmula formal E um exemplo numérico passo a passo, o que ajuda a fixar o conceito
- Usou uma questão real de concurso (Casa da Moeda 2024), aumentando a relevância
- Comparou com juros simples, reforçando a diferença entre os dois regimes
- Conferi a conta manualmente e o resultado bateu (R$ 20.606,02)

**Dificuldades / observações:**
- Nenhuma dificuldade nesse prompt — resposta completa na primeira tentativa

### Prompt 2: "Explique a diferença entre Tabela SAC e Tabela PRICE com um exemplo numérico"

**Resposta obtida (resumo):**
A IA explicou que no SAC a amortização é fixa e a prestação é decrescente (pois os juros incidem sobre um saldo devedor cada vez menor), enquanto no PRICE a prestação é fixa e a amortização cresce ao longo do tempo. Trouxe um exemplo numérico comparativo completo: empréstimo de R$ 120.000,00 a 10% ao mês em 4 parcelas, com tabela mês a mês para os dois sistemas.

**O que funcionou bem:**
- Apresentou as duas tabelas lado a lado, facilitando a comparação visual
- Explicou o "porquê" de cada comportamento (não só o cálculo, mas a lógica por trás)
- Resumo final direto, bom para revisão rápida antes da prova

**Dificuldades / observações:**
- Na tabela do PRICE, o saldo final do último mês deu R$ 7,79 ao invés de zero exato (erro de arredondamento acumulado ao longo das parcelas) — é importante sempre conferir os números gerados pela IA manualmente, especialmente em cálculos com várias casas decimais

### Prompt 3: "Na tabela do sistema PRICE que você gerou, o saldo final do 4º mês deu R$ 7,79 ao invés de zero. Por que isso aconteceu e qual seria o valor exato da prestação para zerar o saldo?"

**Contexto:** prompt de troubleshooting, feito em cima de uma inconsistência identificada na resposta do Prompt 2 (saldo final não zerado devido a arredondamento).

**Resposta obtida (resumo):**
A IA explicou que o resíduo veio do uso de um valor aproximado de prestação (R$37.854,82), e que pequenas diferenças de centavos se acumulam ao longo dos meses por causa do efeito de juros compostos. Recalculou a prestação usando a fórmula exata de anuidades do sistema PRICE, chegando a R$ 37.856,50, e apresentou uma nova tabela onde o saldo final do 4º mês efetivamente zera.

**O que funcionou bem:**
- A IA identificou corretamente a causa do erro (arredondamento acumulado), sem inventar uma justificativa errada
- Apresentou a fórmula formal do sistema PRICE (fórmula de anuidades), que não havia aparecido no prompt anterior
- Corrigiu a tabela e o saldo final bateu certinho em R$ 0,00

**Dificuldades / observações:**
- Esse é um bom exemplo de "cicatriz" real: a resposta inicial (Prompt 2) trouxe um pequeno erro numérico que só foi percebido com conferência manual — reforça a importância de sempre validar resultados numéricos gerados pela IA antes de usá-los para estudo
- Prompt de acompanhamento (follow-up) funcionou melhor que pedir tudo de uma vez: separar "explicação + exemplo" do "correção do erro" trouxe respostas mais precisas

## 4. Miniguia de Estudo (Entrega Final)

### Resumo estruturado

**Juros Compostos**
- Taxa incide sobre o capital acumulado (juros sobre juros)
- Crescimento exponencial do montante
- Fórmula: M = C · (1 + i)^n

**Sistema SAC (Amortização Constante)**
- Amortização fixa a cada parcela
- Prestação decrescente (juros caem porque o saldo devedor cai)
- Fórmula da amortização: A = Valor do Empréstimo / Número de Prestações

**Sistema PRICE (Sistema Francês)**
- Prestação fixa durante todo o contrato
- Amortização crescente (começa menor, termina maior)
- Fórmula: P = C · [i(1+i)^n] / [(1+i)^n − 1]

**Atenção:** cálculos com prestação arredondada podem gerar resíduo no saldo final — 
sempre prefira a fórmula exata ao invés de aproximações.

### Glossário

| Termo | Definição |
|---|---|
| Montante | Valor final de um capital após incidência dos juros |
| Capital | Valor inicial aplicado ou emprestado |
| Taxa de juros | Percentual cobrado/rendido sobre o capital em cada período |
| Amortização | Parte da prestação destinada a reduzir o valor da dívida (principal) |
| Saldo devedor | Valor da dívida ainda não quitado |
| SAC | Sistema de Amortização Constante — amortização fixa, prestação decrescente |
| PRICE | Sistema Francês de Amortização — prestação fixa, amortização crescente |

### Prompts reutilizáveis para revisão
- "Explique [conceito] com um exemplo prático de concurso bancário"
- "Crie um quiz de 5 questões de múltipla escolha sobre [tema], no estilo CESGRANRIO"
- "Compare [conceito A] e [conceito B] com exemplo numérico"
- "Revise esta minha resolução de [questão] e aponte se há algum erro de cálculo"
