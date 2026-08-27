# dashboard-faturamentodireto
# FTD Dashboard

Dashboard de controle de lançamentos e verificações financeiras, com visão geral de erros, valores em risco e acurácia dos dados por obra.

## Sobre o projeto

O FTD Dashboard é uma interface para acompanhar a saúde dos lançamentos financeiros importados (ex: ftdData.json), destacando:

- Volume total de lançamentos e valor movimentado
- Lançamentos validados (OK) vs. lançamentos com erro
- Valor financeiro em risco por causa de divergências
- Acurácia geral dos dados, com indicador visual de status
- Distribuição dos tipos de erro mais comuns (ex: CNPJ divergente, data divergente)
- Ranking de obras por quantidade de erros, valor total ou ordem alfabética
- Alertas automáticos apontando o problema mais crítico do momento

## Funcionalidades

- Cards de resumo: total de lançamentos, valor total, lançamentos OK, erros encontrados, valor em risco e acurácia geral
- Gráfico de rosca (donut chart) com a distribuição percentual dos tipos de erro
- Tabela de obras com filtros (Mais erros / Maior valor / A-Z) e barra de indicador de saúde por obra
- Banner de alerta destacando o erro mais frequente
- Card de alerta flutuante com resumo do impacto financeiro e da obra mais crítica, podendo ser fechado
- Layout responsivo, adaptado para desktop, tablet e mobile

## Como usar

Este projeto e um unico arquivo estatico, sem dependencias ou build necessario.

1. Clone o repositorio:

   git clone https://github.com/fabriciocavalcante0608-ops/ftd-dashboard.git
   cd ftd-dashboard

2. Abra o arquivo ftd-dashboard.html diretamente no navegador:

   macOS: open ftd-dashboard.html
   Windows: start ftd-dashboard.html
   Linux: xdg-open ftd-dashboard.html

   Ou use uma extensao como Live Server (VS Code) para servir o arquivo localmente.

## Estrutura do projeto

ftd-dashboard/
  ftd-dashboard.html   (pagina unica com HTML, CSS e JS)
  README.md

## Dados

Atualmente os dados das obras sao carregados de um array JavaScript embutido no arquivo (variavel "obras"), simulando o conteudo de um arquivo como ftdData.json. Para conectar a dados reais:

1. Substitua o array "obras" no script pela leitura de um arquivo JSON real (via fetch) ou por uma chamada a uma API.
2. Ajuste os cards de resumo (Total de Lancamentos, Valor Total, Erros Encontrados, etc.) para calcular os valores dinamicamente a partir dos dados carregados, em vez de valores fixos no HTML.
3. Recalcule os percentuais do grafico de rosca com base na contagem real de cada tipo de erro.

## Tecnologias

- HTML5 - estrutura semantica
- CSS3 - variaveis CSS, grid, flexbox, media queries
- JavaScript (vanilla) - renderizacao dinamica da tabela de obras
- SVG - grafico de rosca desenhado nativamente, sem bibliotecas externas


