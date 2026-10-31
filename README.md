# Organizador de Informações para o Imposto de Renda

Projeto desenvolvido para o desafio da [DIO](https://www.dio.me/) com o objetivo de criar uma ferramenta prática no Excel para reunir, padronizar e revisar informações utilizadas na preparação da declaração de Imposto de Renda.

A planilha foi construída para transformar vários registros dispersos em uma visão organizada: o usuário cadastra rendimentos, despesas e bens; utiliza campos padronizados; acompanha os totais no resumo; e verifica os documentos pendentes no checklist.

> **Atenção:** este projeto é uma ferramenta de organização. Ele não substitui o programa oficial da Receita Federal nem a orientação de um profissional contábil.

## Visão geral

 <img width="1860" height="891" alt="image" src="https://github.com/user-attachments/assets/d73831a9-f7cb-4661-96cb-93ff5f78bcbd" />




## O que o projeto resolve

Uma declaração de Imposto de Renda exige informações de diferentes fontes, como informes de rendimentos, comprovantes de despesas, documentos de bens e dados bancários. Sem uma estrutura de controle, é fácil esquecer documentos, repetir lançamentos ou perder a visão dos totais.

Esta solução organiza esse processo em uma única pasta de trabalho, com:

- áreas separadas para cada tipo de informação;
- menus suspensos para padronizar categorias;
- cálculos automáticos no resumo;
- checklist de documentos;
- identificação visual de campos editáveis;
- gráfico para visualizar a distribuição das despesas.

## Estrutura da pasta de trabalho

| Aba | Função |
|---|---|
| **Início** | Apresenta o objetivo da ferramenta e orienta o preenchimento. |
| **Resumo** | Exibe totais, controles de preenchimento e o gráfico de despesas. |
| **Rendimentos** | Registra salários, aluguéis, pró-labore, aposentadoria, trabalho autônomo e outras receitas. |
| **Despesas** | Registra despesas, documentos, valores pagos e indicação de dedutibilidade. |
| **Bens** | Registra imóveis, veículos, investimentos, contas, participações e outros direitos. |
| **Checklist** | Controla documentos pendentes e a revisão final. |
| **Listas** | Mantém os valores utilizados nas validações dos menus suspensos. |

## Como utilizar

1. Abra o arquivo `Agregador_IR_DIO.xlsx` no Microsoft Excel.
2. Leia as orientações na aba **Início**.
3. Substitua ou exclua os registros identificados como **Exemplo**.
4. Cadastre cada rendimento, despesa ou bem em uma linha.
5. Use os menus suspensos para selecionar categorias e status.
6. Informe os documentos e mantenha as observações quando necessário.
7. Atualize o **Checklist** conforme reunir os comprovantes.
8. Revise os totais e os alertas na aba **Resumo**.

Os registros de exemplo servem apenas para demonstrar o funcionamento das fórmulas. Eles não representam dados reais e não devem ser usados em uma declaração.

## Recursos técnicos utilizados

- Validação de dados com listas suspensas.
- Fórmulas `SUM`, `SUMIF`, `COUNTIF`, `COUNTIFS`, `COUNTBLANK` e `IF`.
- Formatação monetária e de datas.
- Formatação condicional para os status do checklist.
- Congelamento dos cabeçalhos nas abas de lançamento.
- Gráfico de rosca com despesas por categoria.
- Resumo vinculado diretamente às áreas de entrada.
- Gridlines ocultas e organização visual por função.

## Lógica do resumo

O resumo é alimentado diretamente pelas abas de cadastro:

- **Rendimentos registrados:** conta os registros identificados na aba `Rendimentos`.
- **Rendimentos totais:** soma os valores cadastrados na coluna de valor.
- **Despesas registradas:** conta os registros identificados na aba `Despesas`.
- **Despesas dedutíveis:** soma somente os lançamentos marcados como `Sim`.
- **Patrimônio final:** soma os valores finais informados na aba `Bens`.
- **Campos obrigatórios vazios:** identifica registros preenchidos sem documento informado.

Essa estrutura mantém os cálculos visíveis e permite que o usuário acompanhe de onde cada resultado foi obtido.

## Organização do repositório

```text
.
├── Agregador_IR_DIO.xlsx
├── README.md
└── images
    ├── visao-inicio.png
    └── visao-resumo.png
```

## Validações realizadas

- Conferência dos principais totais da aba `Resumo`.
- Verificação das fórmulas e referências entre as abas.
- Busca por erros como `#REF!`, `#VALUE!`, `#DIV/0!` e `#N/A`.
- Revisão visual da tela inicial e do resumo.
- Teste das listas de validação e dos status do checklist.

## Limitações

A planilha não interpreta automaticamente todas as regras tributárias, não importa dados diretamente de bancos ou da Receita Federal e não calcula a declaração completa. O usuário deve revisar os documentos, os valores e o período correspondente antes de utilizar qualquer informação.



## Autor

**Wellington Vieira Rosa de Souza Junior**

Projeto desenvolvido como parte da formação em dados e Excel na DIO.
