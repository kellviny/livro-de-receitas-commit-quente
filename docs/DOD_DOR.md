# Acordos de Qualidade da Equipe – Commit Quente

Este documento registra os contratos de qualidade (**Definition of Ready** e **Definition of Done**) adotados pela equipe **Commit Quente** para o repositório **Livro de Receitas Colaborativo**, em conformidade com as regras definidas em [CONTRIBUTING.md](../CONTRIBUTING.md).

## Definition of Ready (DoR)

Uma Issue só pode ser assumida por alguém quando:

- [ ] Tem título claro e específico
- [ ] Está escrita no formato **Como** [persona], **quero** [funcionalidade/receita], **para que** [benefício]
- [ ] Indica a persona beneficiada (definida em `docs/PERSONAS.md`)
- [ ] Tem a categoria definida quando aplicável (`saladas`, `carnes`, `sopas`, `massas` ou `sobremesas`)
- [ ] Tem pelo menos 2 critérios de aceitação verificáveis em checklist (`- [ ]`)
- [ ] Tem a label adequada (`user-story` ou `enhancement`) e referência explícita ao épico pai (ex.: `Parte do Épico #X`)

## Definition of Done (DoD)

Uma entrega só está concluída quando:

- [ ] Foi desenvolvida em branch própria seguindo o padrão do repositório (`feature/<categoria>-<nome-da-receita>`, `fix/...` ou `docs/...`)
- [ ] Segue o template obrigatório de receita definido em [CONTRIBUTING.md](../CONTRIBUTING.md) (`# Nome da Receita`, `## Ingredientes`, `## Modo de Preparo` e links de navegação)
- [ ] O índice [menu.md](../menu.md) foi atualizado com o link da entrega (quando aplicável)
- [ ] Todos os links foram testados e funcionam corretamente
- [ ] O texto foi revisado e está sem erros de ortografia ou formatação Markdown
- [ ] Os commits seguem o padrão *Conventional Commits* (`feat:`, `docs:`, `fix:`, `refactor:`, `test:`, `chore:`)
- [ ] Todos os critérios de aceitação da Issue foram atendidos e o Pull Request referencia a Issue (`Closes #X`)
- [ ] O Pull Request tem no mínimo **3 aprovações** de integrantes distintos (mesma regra configurada na proteção da `main`)
- [ ] O merge na `main` foi feito sem conflitos e a branch remota foi removida
