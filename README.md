# Dashboard de Vendas Porsche

Dashboard interativo desenvolvido em **HTML, CSS e JavaScript**, com base na planilha `PlanilhaPorscheSanitizadaFinal.xlsx`. O projeto foi criado para explorar os dados de vendas, acompanhar indicadores e responder perguntas de negócio por meio de gráficos e filtros.

## Objetivos

- Apresentar uma visão executiva das vendas.
- Permitir recortes dos dados por características dos veículos e das operações.
- Responder a três perguntas de negócio relevantes.
- Facilitar a consulta dos registros e a exportação dos dados filtrados.

## Conteúdo do dashboard

### Indicadores principais

- **Vendas filtradas:** quantidade de registros que atendem aos filtros selecionados.
- **Receita registrada:** soma dos preços dos veículos nos registros selecionados.
- **Ticket médio:** receita registrada dividida pela quantidade de registros.
- **Entregues:** percentual e quantidade de registros cujo status é `Delivered`.

### Perguntas de negócio

1. **Quais modelos geram mais receita?**  
   O gráfico classifica os modelos pela soma dos preços registrados. Pode apoiar discussões sobre mix de produtos e prioridades comerciais.

2. **Quais estados concentram as vendas?**  
   O gráfico compara a quantidade de registros por estado. Ajuda a identificar a concentração geográfica presente na base analisada.

3. **Como estão as vendas e as entregas?**  
   O gráfico apresenta a distribuição por status operacional, permitindo acompanhar entregas concluídas, operações em andamento e cancelamentos.

### Análise complementar

O dashboard também mostra a distribuição por método de pagamento, para visualizar a frequência de cada opção na base.

## Filtros disponíveis

Os gráficos, indicadores e a tabela são atualizados de acordo com os filtros selecionados:

- **Modelo:** modelo Porsche.
- **Estado:** estado associado ao registro.
- **Cidade:** cidade associada ao registro.
- **Ano do veículo:** ano do modelo.
- **Pagamento:** método de pagamento.
- **Status da entrega:** situação operacional do registro.

O filtro de cidade acompanha o estado selecionado. Use **Limpar filtros** para voltar à visão completa.

## Tabela e exportação

A seção **Registros da seleção** exibe os registros que correspondem aos filtros aplicados. O botão **Exportar CSV** baixa os registros filtrados em um arquivo CSV, que pode ser aberto em programas como Excel.

## Como executar

O dashboard é um arquivo HTML único, com os dados incorporados e sem dependências externas necessárias para a visualização.

1. Baixe ou copie `index.html` para uma pasta local.
2. Abra o arquivo com um navegador atualizado, como Google Chrome, Microsoft Edge ou Firefox.
3. Selecione os filtros para explorar os dados.

Não é necessário instalar Python, configurar um servidor ou conectar o arquivo ao Excel para executar a versão local.

## Publicação na web

Para compartilhar o dashboard por um link público, publique o arquivo HTML em um serviço de hospedagem de páginas estáticas. O arquivo atual funciona localmente; a criação de um link público depende dessa etapa de hospedagem.

## Fonte dos dados e qualidade

- **Arquivo de origem:** `PlanilhaPorscheSanitizadaFinal.xlsx`
- **Aba utilizada:** `Sanitized`
- **Registros incorporados:** 100

A base contém **24 datas marcadas como `INVALID`**. O dashboard apresenta esses casos como “Data inválida” na tabela e não utiliza essas datas em análises temporais.

## Como interpretar os indicadores

- A **receita registrada** corresponde à soma dos preços presentes nos registros selecionados. Não deve ser interpretada automaticamente como receita contábil reconhecida.
- O cálculo inclui registros de todos os status, inclusive operações em andamento ou canceladas. Para análises financeiras oficiais, defina previamente as regras de reconhecimento de receita.
- O **ticket médio** é calculado dividindo a soma dos preços pela quantidade de registros selecionados.
- A quantidade por estado representa a distribuição dentro desta planilha, não a participação de mercado real.
- Os valores monetários são formatados em **USD** no dashboard. Confirme a moeda original da fonte antes de utilizar os valores em relatórios financeiros.

## Tecnologias utilizadas

- **HTML5:** estrutura da página.
- **CSS3:** identidade visual responsiva e layout.
- **JavaScript:** filtros, cálculos dos indicadores, gráficos em canvas, tabela e exportação CSV.

## Estrutura do projeto

```text
dashboard-porsche/
├── index.html
└── README.md
```

O HTML contém a estrutura, os estilos, o código JavaScript e os dados usados pela dashboard.

## Possíveis melhorias futuras

- Criar análises temporais depois de corrigir ou validar as datas inválidas.
- Adicionar comparação de receita por estado e método de pagamento.
- Incluir metas comerciais e comparação entre períodos.
- Desenvolver uma versão com visual semelhante ao Power BI.
- Automatizar a atualização do dashboard a partir de uma nova planilha.
- Publicar a página com URL própria e configurar um processo simples de atualização.

---

**Projeto:** Dashboard de Vendas Porsche  
**Idioma:** Português (Brasil)  
**Tipo:** Dashboard estático e interativo em arquivo HTML único
