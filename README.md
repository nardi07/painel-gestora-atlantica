# Painel Gestora Atlântica

Painel interativo de KPIs para uma gestora de investimentos **fictícia**, feito como projeto de portfólio.

🔗 **Ver o painel:** https://nardi07.github.io/painel-gestora-atlantica/

## O que o painel mostra

- **Grandes números:** PL sob gestão (R$ 77,9 bi), captação líquida, receita de taxas, rentabilidade, % do CDI e número de cotistas, com variação vs ano anterior e atingimento de meta.
- **Comparação com o CDI:** rentabilidade da carteira mês a mês contra o CDI e desempenho de cada classe e fundo em % do CDI.
- **Visão temporal:** evolução por mês, trimestre ou ano, comparando com o ano anterior, o período anterior, a meta ou o CDI.
- **Filtros cruzados:** período, classe de ativo, canal de distribuição, região e fundo. Clicar numa barra ou linha da tabela filtra o painel inteiro.
- **Resumo automático** em texto, mapa de calor de captação por classe e tabela de fundos ordenável.
- **Copiar link da visão:** gera um link que reabre o painel com os mesmos filtros.
- Exportação dos dados filtrados em CSV, impressão/PDF e tema claro/escuro.

## Como foi feito

- **Dados:** 36 meses (out/23 a set/26) de 20 fundos em 7 classes, 4 canais e 5 regiões, gerados com Python (pandas/NumPy). A curva do CDI segue de forma aproximada o caminho da Selic no período; fundos e valores são fictícios.
- **Métricas:** saldos (PL, cotistas) usam o valor do último mês do intervalo; taxas (rentabilidade, % do CDI) são calculadas como soma/soma, nunca média de percentuais.
- **Painel:** um único arquivo HTML com JavaScript e SVG puros, sem bibliotecas externas. Funciona offline e é responsivo até a tela do celular.
- **Validação:** KPIs conferidos contra os totais calculados no pandas; renderização testada em desktop, celular e tema escuro com Playwright.

> Todos os dados são fictícios e servem apenas para demonstração.
