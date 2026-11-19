# Livro de Receitas – Commit Quente

Coleção colaborativa de receitas navegável em Markdown, desenvolvida pela equipe **Commit Quente** para a atividade prática de Gerência de Configuração de Software (SCM) com Git e GitHub.

## Sumário

- [Sobre o Projeto](#sobre-o-projeto)
- [Estrutura de Categorias](#estrutura-de-categorias)
- [Como Navegar](#como-navegar)
- [Como Contribuir](#como-contribuir)
- [Integrantes](#integrantes)

## Sobre o Projeto

Este repositório reúne receitas organizadas por categoria, aplicando na prática os conceitos de controle de versão, *GitHub Flow*, *issues*, *Pull Requests*, revisão por pares (*Code Review*) e proteção da branch `main`.

## Estrutura de Categorias

```text
.
├── README.md
├── CONTRIBUTING.md
├── menu.md
├── saladas/
├── carnes/
├── sopas/
├── massas/
└── sobremesas/
```

- **Saladas** (`saladas/`)
- **Carnes** (`carnes/`)
- **Sopas** (`sopas/`)
- **Massas** (`massas/`)
- **Sobremesas** (`sobremesas/`)

## Como Navegar

1. Acesse o índice principal em [menu.md](menu.md) para visualizar todas as categorias e receitas disponíveis.
2. Ou clone o repositório localmente:
   ```bash
   git clone https://github.com/kellviny/livro-de-receitas-commit-quente.git
   ```

## Como Contribuir

Todas as contribuições devem ser feitas via *Issue*, *Feature Branch* e *Pull Request* — **commits diretos na `main` são bloqueados**.

Resumo do fluxo:
1. Abra uma *Issue* descrevendo a receita e a categoria (ex.: `[Receita] Pudim de Leite - Sobremesas`).
2. Crie uma branch a partir da `main` atualizada: `feature/<categoria>-<nome-da-receita>`.
3. Adicione a receita na pasta da categoria e atualize o [menu.md](menu.md) usando *Conventional Commits* (`feat:`, `docs:`).
4. Abra um *Pull Request* referenciando a *Issue* (`Closes #X`) e aguarde **no mínimo 3 aprovações** antes do merge.

Para o guia completo de padrões e regras, consulte o arquivo [CONTRIBUTING.md](CONTRIBUTING.md).

## Integrantes

- **Product Owner:** Kellviny — [@kellviny](https://github.com/kellviny)
- **Colaborador:** Fredson Medeiros — [@fredszn](https://github.com/fredszn)
- **Colaboradora:** Isabele Rodrigues de Souza — [@isarodrr](https://github.com/isarodrr)
- **Colaborador:** Thalyson — [@ThalysonWh](https://github.com/ThalysonWh)
- **Colaborador:** Luiz Neto — [@luizneto010101](https://github.com/luizneto010101)