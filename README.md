# 📘 Guia Completo de Comandos Git

Este repositório tem como objetivo servir como **guia completo e prático de comandos Git**, desde o primeiro contato (inicialização) até fluxos mais avançados de trabalho. Ideal para estudantes, iniciantes e também para consulta rápida no dia a dia.

---

## 📌 O que é o Git?

O **Git** é um sistema de controle de versão distribuído que permite registrar alterações em arquivos, colaborar em equipe e manter o histórico completo de um projeto.

---
## 🚨 Conflitos

Quando usamos um repositorio local desatualizado podemos cair em varios problemas de conflitos ao salvar os arquivos para o repositorio local.

### Caso de um conflito em arquivos diferentes basta executar esses comandos

```bash
git pull origin main
```
colocar o commit pelo VIM
```bash
git push
```

### Caso de um conflito em arquivos **iguais** basta executar esses comandos

```bash
git pull origin main
```
Entrar no Codigo e decidir qual ira permanecer
```bash
git add .
git commit -m "comentario"
git push
```

### Caso de um upload de arquivos forçados, removendo tudo do repositorio remoto e suindo somente os arquivos do repositorio local
```bash
git push -f
```

---

## 🚀 Configuração Inicial do Git

### Verificar se o Git está instalado

```bash
git --version
```

### Configurações básicas (obrigatórias)

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@email.com"
```

### Ver todas as configurações

```bash
git config --list
```

---

## 📂 Iniciando um Repositório

### Criar um novo repositório Git

```bash
git init
```

### Clonar um repositório existente

```bash
git clone https://github.com/usuario/repositorio.git
```

---

## 📄 Trabalhando com Arquivos

### Ver status do repositório

```bash
git status
```

### Adicionar arquivos ao stage

```bash
git add arquivo.txt
git add .
```

### Remover arquivos do stage

```bash
git restore --staged arquivo.txt
```

---

## 💾 Commits

### Criar um commit

```bash
git commit -m "mensagem do commit"
```

### Commit direto (add + commit)

```bash
git commit -am "mensagem"
```

### Alterar último commit

```bash
git commit --amend
```

---

## 📜 Histórico e Logs

### Ver histórico de commits

```bash
git log
```

### Histórico resumido

```bash
git log --oneline
```

### Histórico com gráfico

```bash
git log --oneline --graph --all
```

---

## 🌿 Branches

### Listar branches

```bash
git branch
```

### Criar uma branch

```bash
git branch nome-da-branch
```

### Trocar de branch

```bash
git checkout nome-da-branch
```

### Criar e trocar de branch

```bash
git checkout -b nova-branch
```

### Deletar branch

```bash
git branch -d nome-da-branch
```

---

## 🔀 Merge e Rebase

### Fazer merge

```bash
git merge nome-da-branch
```

### Rebase

```bash
git rebase nome-da-branch
```

---

## 🌍 Repositórios Remotos

### Ver repositórios remotos

```bash
git remote -v
```

### Adicionar repositório remoto

```bash
git remote add origin https://github.com/usuario/repositorio.git
```

### Enviar commits (push)

```bash
git push origin main
```

### Baixar alterações (pull)

```bash
git pull origin main
```

### Buscar alterações sem aplicar

```bash
git fetch
```

---

## ⏪ Desfazendo Alterações

### Descartar alterações locais

```bash
git restore arquivo.txt
```

### Voltar para um commit específico

```bash
git checkout hash_do_commit
```

### Reset

```bash
git reset --soft HEAD~1
git reset --mixed HEAD~1
git reset --hard HEAD~1
```
### Limpa os arquivos novos

```bash
git clean -df
```
### Limpa as modificações 

```bash
git checkout -- .
```

---

## ⚙ Editor VIM

### habilitar modo de edicao

```bash
i
```
### Sair do VIM salvando alteracoes 

```bash
<ESC>
:wq
<ENTER>
```
### Sair do VIM descartando alteracoes 

```bash
<ESC>
:q!
<ENTER>
```
---

## 🧹 Stash (Guardar alterações temporárias)

### Salvar alterações

```bash
git stash
```

### Listar stash

```bash
git stash list
```

### Recuperar stash

```bash
git stash pop
```

---

## 🏷️ Tags

### Criar tag

```bash
git tag v1.0
```

### Enviar tags

```bash
git push origin --tags
```

---

## 🔒 .gitignore

Arquivo usado para ignorar arquivos e pastas:

```
node_modules/
.env
*.log
```

---

## 📦 Fluxo Básico de Trabalho

```text
Editar arquivos
→ git status
→ git add .
→ git commit -m "mensagem"
→ git pull
→ git push
```

---

## 📚 Comandos Úteis

```bash
git diff
git show
git blame arquivo.txt
git shortlog
git reflog
```

---

## ✅ Boas Práticas

* Commits pequenos e frequentes
* Mensagens claras e objetivas
* Sempre usar branches
* Evitar commit direto na `main`

Se este guia te ajudou, ⭐ o repositório!
