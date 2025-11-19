## Resolução de Conflitos e Reversão de Commits

### Resolução de Conflitos

Quando duas branches alteram a mesma linha de um arquivo, um conflito de merge pode ocorrer. O processo recomendado é:

1. Realizar o merge normalmente (`git merge nome-da-branch`)
2. O Git irá sinalizar o(s) arquivo(s) em conflito, marcando as regiões conflitantes
3. Editar o(s) arquivo(s) para manter, descartar ou combinar as alterações, conforme decisão do time
4. Após resolver, salvar o arquivo, adicionar com `git add nome-do-arquivo` e finalizar com `git commit`
5. O commit de resolução deve ser elucidativo, explicando como o conflito foi resolvido

**Exemplo de mensagem:**
```bash
ui(index): resolve conflito de merge combinando títulos das branches ui/titulo-novo e ui/titulo-destaque
```

### Reversão de Commit

Se for necessário desfazer um commit já integrado (sem apagar o histórico), utilize:

```bash
git revert hash-do-commit
```
Isso cria um novo commit que desfaz as alterações do commit anterior, mantendo o histórico transparente.

**Exemplo de mensagem:**
```bash
revert: desfaz alteração do título principal para restaurar versão anterior
```

> Sempre documente no Pull Request ou no commit o motivo da reversão.
# Workflow Oficial – Sebo Online

## Modelo Adotado

Adotaremos uma variação do **GitHub Flow**, adaptada para o contexto do Sebo Online, priorizando simplicidade, colaboração e integração contínua.

## GitHub Flow

- **Branch principal:** `main`
- **Branches de funcionalidades:** criadas a partir de `main` para cada nova feature, correção ou melhoria.
- **Pull Requests:** toda integração na `main` deve ser feita via Pull Request, com revisão obrigatória.

## Estratégia de Branches

- **main:** branch principal, sempre estável e pronta para deploy.
- **feature/nome-da-feature:** para desenvolvimento de novas funcionalidades.
- **fix/nome-do-bug:** para correções de bugs.
- **hotfix/nome-do-hotfix:** para correções urgentes em produção.
- **docs/nome-da-doc:** para alterações exclusivas de documentação.

### Origem e Destino dos Merges
- Branches são criadas a partir de `main`.
- Merges sempre têm como destino a `main`.
- Utilizar Pull Request para todo merge, com revisão obrigatória.

## Regras de Atualização

- Atualizar a branch `main` apenas após aprovação de Pull Request.
- Antes de abrir um Pull Request, atualizar sua branch local com `git pull origin main` e resolver conflitos.
- Deploys só podem ser feitos a partir da `main`.

## Política de Revisão e Integração

- Todo código deve ser revisado por pelo menos um membro do time.
- Revisores devem verificar clareza, testes, impacto e aderência ao padrão de commits.
- Integração só após aprovação e build/testes automatizados.

## Política de Commits Semânticos

Adotamos o padrão:

```
tipo(escopo opcional): descrição
```

### Tipos Comuns
- **feat:** nova funcionalidade
- **fix:** correção de bug
- **docs:** documentação
- **refactor:** refatoração sem alterar funcionalidade
- **style:** ajustes de formatação/estilo
- **test:** adição/refatoração de testes
- **chore:** tarefas de manutenção

### Tipos Inéditos do Sebo Online
- **ui:** alterações visuais ou de layout (ex: ajuste em cards de produtos)
- **seo:** melhorias de SEO (ex: meta tags, sitemap)
- **data:** manipulação/importação/exportação de dados (ex: script de migração de categorias)

### Quando Usar Cada Tipo
- **feat:** para adicionar seções como "produtos raros" ou "categorias".
- **fix:** corrigir bugs em listagens ou filtros.
- **docs:** atualizar o README ou este WORKFLOW.md.
- **refactor:** melhorar código sem mudar comportamento.
- **style:** padronizar espaçamento, aspas, etc.
- **test:** criar ou ajustar testes automatizados.
- **chore:** atualizar dependências, configs, .gitignore.
- **ui:** alterar layout, cores, responsividade.
- **seo:** adicionar tags, melhorar acessibilidade para buscadores.
- **data:** scripts de importação/exportação, ajustes em seeders.

## Referências
- [GitHub Flow](https://docs.github.com/en/get-started/quickstart/github-flow)
- [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/)

---

> Mantenha este documento atualizado conforme o time evoluir!
