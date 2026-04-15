#  Guia Completo de Git e Conventional Commits



## Git Commands Guide

A seguir, um guia abrangente de comandos Git, organizados por categoria — do básico ao avançado — para uso no terminal ou integrado a plataformas como o **GitHub**.

---

###  Commit Padrão

```bash
git add .
```
```bash
git status
```
```bash
git commit -m "Mensagem"
```
```bash
git push -u origin main
```

#### Tipos mais utilizados de commit:

| Tipo         | Descrição                                    | Exemplo                                         |
| ------------ | -------------------------------------------- | ----------------------------------------------- |
| **feat**     | Adição de um novo recurso ou funcionalidade. | `feat: adicionar tela de login`                 |
| **fix**      | Correção de um bug.                          | `fix: corrigir erro de autenticação`            |
| **docs**     | Alterações na documentação.                  | `docs: atualizar README com instruções`         |
| **style**    | Mudanças de estilo que não afetam o código.  | `style: ajustar indentação e espaçamento`       |
| **refactor** | Refatoração sem mudança de funcionalidade.   | `refactor: otimizar função de carregamento`     |
| **test**     | Adição ou ajuste de testes automatizados.    | `test: adicionar testes para componente Header` |
| **chore**    | Tarefas gerais de manutenção.                | `chore: atualizar dependências do projeto`      |

---

## 🛠️ Configuração Inicial

* `git config --global user.name "Seu Nome"` — Define o nome do usuário.
* `git config --global user.email "seu@email.com"` — Define o e-mail do usuário.
* `git config --global core.editor "nome_do_editor"` — Define o editor padrão (`vim`, `nano`, etc).
* `git config --list` — Lista todas as configurações atuais.
* `git config --global --list` — Lista todas as configurações do Git definidas no nível global

---

## 📁 Iniciando e Clonando Repositórios

* `git init` — Inicializa um novo repositório Git local.
* `git clone https://github.com/usuario/repositorio.git` — Clona um repositório remoto existente.

---

## 📄 Trabalhando com Arquivos

* `git status` — Mostra o status dos arquivos no diretório de trabalho.
* `git add arquivo.txt` — Adiciona um arquivo específico à área de stage.
* `git add .` — Adiciona todos os arquivos modificados.
* `git commit -m "Mensagem"` — Cria um commit com mensagem descritiva.
* `git commit --amend` — Modifica o último commit.
* `git rm arquivo.txt` — Remove um arquivo do repositório.
* `git mv arquivo_antigo.txt novo_arquivo.txt` — Renomeia ou move um arquivo.

---

## 🔄 Sincronização com Repositórios Remotos

* `git remote -v` — Verifica o repositório remoto configurado.
* `git remote remove origin` — Remove o repositório remoto configurado.
* `git remote add origin https://github.com/usuario/repositorio.git` — Define o repositório remoto.
* `git push -u origin main` — Envia alterações para o remoto.
* `git pull origin main` — Atualiza o repositório local.
* `git push --force` — Força envio de alterações (use com cautela).
* `git fetch` — Baixa alterações do remoto sem mesclar.
* `git remote prune origin` — Remove branches remotas inexistentes.

---

## 📌 Arquivo `.gitignore`

Ignora arquivos ou pastas que não devem ser versionados.

**Exemplo de `.gitignore`:**

```text
# Arquivos de sistema
.DS_Store
Thumbs.db

# Dependências
node_modules/
vendor/

# Arquivos de ambiente
.env
!.env.example
```

---

## 🌿 Gerenciamento de Branches

* `git branch` — Lista branches locais.
* `git branch -a` — Lista todas as branches (locais e remotas).
* `git branch nome-da-branch` — Cria uma nova branch.
* `git checkout nome-da-branch` — Troca de branch.
* `git checkout -b nova-branch` — Cria e entra em uma nova branch.
* `git merge nome-da-branch` — Mescla uma branch na atual.
* `git branch -d nome-da-branch` — Exclui uma branch local.
* `git push origin --delete nome-da-branch` — Exclui branch remota.

---

## 🕵️ Visualização e Histórico

* `git log` — Exibe o histórico completo.
* `git log --oneline` — Histórico resumido.
* `git log --graph --oneline --all` — Histórico em forma de gráfico.
* `git diff` — Mostra as diferenças entre commits.
* `git show` — Exibe detalhes de um commit específico.

---

## 🧪 Stash e Recuperação

* `git stash` — Guarda temporariamente alterações não commitadas.
* `git stash list` — Lista stashes salvos.
* `git stash apply` — Aplica o stash mais recente.
* `git stash drop` — Remove o último stash.
* `git stash clear` — Limpa todos os stashes.

---

## 🧹 Limpeza e Reset

* `git clean -f` — Remove arquivos não rastreados.
* `git reset arquivo.txt` — Remove um arquivo da área de stage.
* `git reset --soft HEAD~1` — Desfaz o último commit mantendo as alterações.
* `git reset --hard HEAD~1` — Desfaz completamente o último commit.

---

## 🔁 Merge e Rebase

* `git merge nome-da-branch` — Junta o histórico de outra branch.
* `git rebase nome-da-branch` — Reaplica commits sobre outra base.
* `git merge --abort` — Cancela um merge em conflito.
* `git rebase --abort` — Cancela um rebase em andamento.

---

## 🏷️ Tags

* `git tag` — Lista tags existentes.
* `git tag -a v1.0 -m "Versão 1.0"` — Cria uma tag anotada.
* `git push origin v1.0` — Envia a tag para o remoto.
* `git tag -d v1.0` — Remove uma tag local.
* `git push origin --delete v1.0` — Remove tag remota.

---

## 🧩 Debug e Diagnóstico

* `git fsck` — Verifica integridade do repositório.
* `git gc` — Otimiza o repositório (garbage collection).
* `git reflog` — Mostra histórico de movimentos do HEAD.
* `git bisect` — Localiza commits que introduziram bugs.

---

## 📦 Patch e Fluxos Alternativos

* `git format-patch` — Gera arquivos de patch a partir de commits.
* `git apply patch-file` — Aplica um arquivo de patch.

---

## 🔍 Ferramentas Adicionais

* `git blame arquivo.txt` — Mostra quem editou cada linha.
* `git shortlog` — Resumo do histórico de commits por autor.
* `git cherry-pick hash` — Aplica um commit específico em outra branch.

---

## 📚 Recursos Recomendados

* [Documentação Oficial do Git](https://git-scm.com/docs)
* [GitHub Education - Git Cheat Sheet (PDF)](https://education.github.com/git-cheat-sheet-education.pdf)
* [Git Reference](https://git.github.io/git-reference/)
