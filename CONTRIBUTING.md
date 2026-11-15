# Guia de Contribuição – Commit Quente

Este documento define os padrões de trabalho, nomenclatura e governança de Gerência de Configuração de Software (SCM) para o projeto **Livro de Receitas – Commit Quente**.

> **Regra de Governança:** Todo PR deve ter no mínimo 3 aprovações antes do merge na main.

---

## 1. Fluxo de Trabalho (GitHub Flow)

A branch `main` é protegida e representa a versão oficial do livro. Commits diretos na `main` são bloqueados.

1. **Abertura de Issue:** antes de escrever uma receita, crie uma *Issue* no GitHub no formato `[Receita] Nome da Receita - Categoria` (ex.: `[Receita] Pudim de Leite - Sobremesas`) e atribua-a a você (*Assignee*).
2. **Atualize a `main` local e crie sua branch:**
   ```bash
   git checkout main
   git pull origin main
   git checkout -b feature/<categoria>-<nome-da-receita>
   ```
3. **Desenvolva e faça commits semânticos:** crie o arquivo da receita e adicione o link dela no [menu.md](menu.md).
4. **Envie a branch para o GitHub:**
   ```bash
   git push -u origin feature/<categoria>-<nome-da-receita>
   ```
5. **Abra um Pull Request (PR):**
   - Base: `main` | Compare: sua branch `feature/...`.
   - Descreva claramente a receita adicionada.
   - Inclua a palavra-chave de fechamento automático da *Issue* (ex.: `Closes #5`).
   - Solicite revisão (*Reviewers*) dos colegas da equipe.
6. **Code Review e Resolução de Conflitos:**
   - Pelo menos **3 integrantes distintos** devem revisar as alterações na aba *Files changed*, validar a formatação Markdown e testar os links antes de aprovar (*Approve*).
   - Se houver conflito no `menu.md` por outro merge anterior, atualize sua branch com a `main`, resolva o conflito e envie o commit de ajuste:
     ```bash
     git pull origin main
     # resolva o conflito no menu.md
     git add menu.md
     git commit -m "fix: resolver conflito no menu.md"
     git push
     ```
7. **Merge e Limpeza:** com as **3 aprovações** concluídas, realize o merge na `main` e exclua a branch remota.

---

## 2. Padrão de Nomenclatura de Branches

| Prefixo | Uso | Exemplo |
| :--- | :--- | :--- |
| `feature/` | Nova receita (padrão obrigatório: `feature/<categoria>-<nome-da-receita>`) | `feature/sobremesas-pudim-de-leite` |
| `fix/` | Correção de erro ou conflito | `fix/link-quebrado-menu` |
| `docs/` | Ajustes apenas de documentação | `docs/atualizar-readme` |

---

## 3. Padrão de Commits (Conventional Commits)

Use prefixos semânticos claros em todas as mensagens de commit:

| Prefixo | Tipo de mudança | Exemplo |
| :--- | :--- | :--- |
| `feat:` | Adição de nova receita | `feat: adicionar receita de pudim de leite` |
| `docs:` | Atualização do `menu.md` ou documentação | `docs: atualizar menu com link para pudim de leite` |
| `fix:` | Correção de links, formatação ou conflitos | `fix: corrigir link da receita no menu.md` |
| `refactor:` | Reorganização sem alterar conteúdo | `refactor: padronizar títulos das receitas` |
| `test:` | Verificações ou testes | `test: validar links do menu` |
| `chore:` | Tarefas de manutenção e configuração | `chore: inicializar estrutura base do livro de receitas` |

---

## 4. Padrão Obrigatório das Receitas

Cada receita deve ser salva em `/<categoria>/<nome-da-receita>.md` (ex.: `sobremesas/pudim-de-leite.md`) seguindo a estrutura abaixo:

```markdown
# Nome da Receita

## Ingredientes
- Ingrediente 1
- Ingrediente 2

## Modo de Preparo
1. Passo 1.
2. Passo 2.

---

[Voltar à Categoria](.) | [Voltar ao Menu Principal](../menu.md)
```

> **Observação:** o arquivo `.gitkeep` dentro de cada pasta de categoria existe apenas para o Git versionar a pasta inicialmente e pode ser removido quando a pasta receber sua primeira receita.
