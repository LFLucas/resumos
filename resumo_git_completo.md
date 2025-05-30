
# ✅ Resumo Completo de Comandos Git

---

## 🔧 Configuração de Usuário (usuario)

`git config --global user.name "nome"`  
Define o nome do usuário globalmente.

`git config --global user.email "email"`  
Define o e-mail do usuário globalmente.

`git config --list`  
Lista todas as configurações (local, global, sistema).

`git config --global --list`  
Lista apenas configurações globais.

---

## 📁 Repositório (repositorio)

`git init`  
Inicia um repositório local.

`git init --bare`  
Cria um repositório sem área de trabalho (para servidores).

`git clone [url].git [pasta]`  
Clona um repositório remoto para uma pasta local.

---

## 🔎 Status e Alterações (status)

`git status`  
Mostra o estado atual dos arquivos.

`git diff`  
Mostra diferenças entre diretório e stage.

`git diff --staged`  
Mostra diferenças entre stage e último commit.

---

## ➕ Adicionar ao Stage (add)

`git add .`  
Adiciona todos os arquivos (modificados e novos).

`git add -A`  
Adiciona arquivos novos, modificados e deletados.

`git add *.ts`  
Adiciona apenas arquivos que terminam com `.ts`.

---

## ➖ Remover do Stage (reset)

`git reset`  
Remove todos os arquivos do stage.

`git reset *.ts`  
Remove apenas arquivos `.ts` do stage.

---

## ♻️ Restaurar Arquivos (restore)

`git restore .`  
Restaura todos os arquivos do diretório de trabalho.

`git restore --staged [arquivo]`  
Remove arquivo do stage, sem apagar mudanças.

`git restore *.ts`  
Restaura apenas arquivos `.ts`.

---

## ✅ Commit (commit)

`git commit -m "mensagem"`  
Cria um commit com os arquivos no stage.

`git commit -a -m "mensagem"`  
Adiciona e commita arquivos rastreados em um só comando.

`git commit --amend -m "nova mensagem"`  
Altera o último commit sem criar um novo.

---

## 📜 Histórico (log)

`git log`  
Mostra todos os commits.

`git log -3`  
Mostra os 3 últimos commits.

`git log --oneline`  
Mostra histórico resumido.

`git log --oneline -5`  
Mostra os 5 últimos commits em uma linha cada.

`git log --graph`  
Mostra histórico com visual de ramificações.

`git log --author="nome"`  
Filtra commits por autor.

`git log --before="YYYY-MM-DD"`  
Filtra commits anteriores a uma data.

`git log --since="data"`  
Filtra commits após uma data.

---

## 📋 Outros Logs (reflog)

`git shortlog`  
Resumo de commits por autor.

`git reflog`  
Mostra todas as ações recentes (commits, checkout, etc).

---

## 🌿 Branches (branch)

`git branch`  
Lista todas as branches.

`git branch [nome]`  
Cria uma nova branch.

`git branch -D [nome]`  
Deleta uma branch.

`git checkout [nome]`  
Muda para outra branch.

`git checkout -b [nova]`  
Cria e muda para nova branch.

`git branch -m [novo_nome]`  
Renomeia a branch atual.

`git log [branch]`  
Mostra o histórico da branch indicada.

`git diff [branch1] [branch2]`  
Mostra diferenças entre duas branches.

---

# 🚀 Comandos Úteis no Dia a Dia (diario)

---

## 🔁 Atualizar Código Local (pull)

`git pull`  
Baixa e mescla alterações da remota com a local.

`git pull --rebase`  
Atualiza reescrevendo seu histórico local por cima do remoto.

---

## ⬆️ Enviar Código ao Repositório (push)

`git push`  
Envia commits locais para o repositório remoto.

`git push -u origin [branch]`  
Envia e define branch remota como padrão.

---

## 🧼 Limpeza de Arquivos (clean)

`git clean -f`  
Remove arquivos não rastreados.

`git clean -fd`  
Remove arquivos e diretórios não rastreados.

---

## 📂 Ver Repositórios Remotos (remote)

`git remote -v`  
Lista repositórios remotos configurados.

`git remote add origin [url]`  
Adiciona repositório remoto chamado `origin`.

---

## 📌 Stash (stash)

`git stash`  
Salva alterações e limpa a árvore de trabalho.

`git stash pop`  
Aplica alterações salvas e remove da pilha.

`git stash list`  
Lista todos os stashes salvos.

---

## 🔍 Pesquisar Histórico (search)

`git log -S"trecho"`  
Mostra commits que alteraram um trecho específico.

`git blame [arquivo]`  
Mostra quem alterou cada linha do arquivo.

---

## 📑 Ver Último Commit (show)

`git show --name-only`  
Mostra arquivos modificados no último commit.

`git show [id_do_commit]`  
Mostra detalhes de um commit específico.

---

## 🧠 Atalhos Mentais (atalhos)

- `add`, `commit`, `push`: fluxo básico.  
- `status`, `diff`: entender o que mudou.  
- `checkout`, `branch`, `merge`: trabalhar com branches.  
- `log`, `reflog`, `blame`: investigar histórico.

---

# 🌐 Resumo: Trabalhando com Repositórios Remotos no Git (remoto)

---

## 🔧 Configuração de Repositório Remoto

`git remote add origin [url]`  
Adiciona um repositório remoto chamado `origin`.

`git remote -v`  
Lista os repositórios remotos configurados.

`git remote remove [nome]`  
Remove um repositório remoto.

`git remote set-url origin [nova_url]`  
Atualiza a URL de um repositório remoto.

---

## 📤 Enviar Código (Push)

`git push`  
Envia a branch atual para o remoto padrão.

`git push -u origin [branch]`  
Envia a branch e define como padrão para futuros pushes.

`git push origin --delete [branch]`  
Remove uma branch remota.

---

## 📥 Atualizar Código Local

`git pull`  
Baixa e mescla as alterações do repositório remoto.

`git pull --rebase`  
Atualiza o código reescrevendo a história local por cima da remota.

`git fetch`  
Baixa as atualizações remotas sem aplicar.

---

## 🔁 Sincronização de Branches

`git branch -r`  
Lista as branches remotas.

`git branch -a`  
Lista todas as branches (locais e remotas).

`git checkout -b [nova_branch] origin/[branch_remota]`  
Cria nova branch local a partir de uma remota.

---

## 🧑‍💻 Configuração de Usuário e Credenciais

`git config user.name "Seu Nome"`  
Define o nome do usuário local.

`git config user.email "seu@email.com"`  
Define o e-mail do usuário local.

`git config --global user.name "Seu Nome"`  
Define o nome do usuário globalmente.

`git config --global user.email "seu@email.com"`  
Define o e-mail do usuário globalmente.

`git config --global credential.helper store`  
Armazena suas credenciais em texto plano.

`git config --global credential.helper cache`  
Armazena as credenciais em cache temporário.

---

## 📌 Exemplo de Fluxo com GitHub

```bash
git init
git remote add origin https://github.com/usuario/repositorio.git
git add .
git commit -m "primeiro commit"
git push -u origin main
```

---

## 🧠 Dicas Rápidas

- Use `pull --rebase` para manter um histórico limpo.
- Use `fetch` se quiser inspecionar antes de aplicar alterações.
- Use `credential.helper store` apenas em máquinas pessoais.
- Você pode ter múltiplos remotos com nomes diferentes (`origin`, `upstream`, etc).
