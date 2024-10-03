# Tutorial de Git: Uso Básico e Intermediário

Este repositório contém um tutorial completo sobre o uso básico e intermediário do Git, uma ferramenta essencial para controle de versão de código. Vamos cobrir os comandos mais importantes para gerenciar seu código de forma eficiente, colaborativa e segura.

## Índice
1. [Introdução](#introdução)
2. [Pré-requisitos](#pré-requisitos)
3. [Instalação](#instalação)
4. [Configuração Inicial do Git](#configuração-inicial-do-git)
5. [Comandos Básicos](#comandos-básicos)
   - `git init`
   - `git status`
   - `git add`
   - `git commit`
   - `git log`
   - `git remote`
6. [Trabalhando com Branches](#trabalhando-com-branches)
   - `git branch`
   - `git checkout`
   - `git merge`
7. [Comandos Intermediários](#comandos-intermediários)
   - `git stash`
   - `git rebase`
   - `git reset`
   - `git revert`
   - `git cherry-pick`
8. [Resolvendo Conflitos](#resolvendo-conflitos)
9. [Colaborando em Repositórios Remotos](#colaborando-em-repositórios-remotos)
   - `git clone`
   - `git pull`
   - `git push`
10. [Considerações Finais](#considerações-finais)

---

## Introdução

O Git é um sistema de controle de versão distribuído amplamente utilizado para gerenciar projetos de software. Este tutorial abrange desde os conceitos e comandos mais básicos até as funcionalidades intermediárias que ajudam a melhorar a produtividade e a colaboração em equipes.

## Pré-requisitos

Antes de iniciar, você precisará de:

- Acesso a um terminal (Windows, macOS ou Linux).
- Git instalado na sua máquina (instruções na seção abaixo).
- Uma conta no GitHub (opcional, mas recomendada para colaboração remota).

## Instalação

### Windows
1. Baixe o [Git para Windows](https://git-scm.com/download/win) e siga as instruções de instalação.
2. Verifique a instalação abrindo o terminal e executando:

```bash
-git --version
```
### Linux
No Ubuntu e distribuições baseadas em Debian:

```bash
sudo apt update
sudo apt install git
```
Verifique a instalação com:

```bash
git --version
```
Configuração Inicial do Git
Antes de começar a usar o Git, configure suas informações de usuário:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu-email@example.com"
```
Essas informações serão usadas para identificar as alterações que você fizer nos repositórios.

## Comandos Básicos
1. Iniciar um repositório Git
Para iniciar o controle de versão em um diretório, use o comando:

```bash
git init
```

2. Verificar o status dos arquivos
O comando git status exibe o status atual do repositório, incluindo arquivos modificados, rastreados e não rastreados:

```bash
git status
```

3. Adicionar arquivos ao estágio (staging area)
Para adicionar um arquivo ou arquivos ao estágio antes de fazer o commit:

```bash
#Git add [nome do arquivo]

git add arquivo.txt

# Ou para adicionar todos os arquivos modificados:
# git add [ponto]

git add .

```

4. Fazer um commit
O commit salva as alterações no histórico do Git:

```bash
git commit -m "Mensagem do commit"
```

5. Visualizar o histórico de commits
Veja os commits anteriores com:

```bash
git log
```

6. Conectar a um repositório remoto
Você pode conectar o repositório local a um repositório remoto, como o GitHub:

```bash
git remote add origin https://github.com/seu-usuario/seu-repositorio.git
```

## Trabalhando com Branches
1. Criar uma nova branch
As branches permitem trabalhar em funcionalidades separadas do projeto:

```bash
git branch nome-da-branch
```

2. Mudar para outra branch
Para alternar entre branches:

```bash
git checkout nome-da-branch
```

3. Mesclar branches
Para mesclar uma branch em outra:

```bash
git merge nome-da-branch
```

## Comandos Intermediários
1. Salvando mudanças temporárias (Stash)
O git stash permite salvar temporariamente modificações no repositório sem fazer um commit:

```bash
git stash
```

2. Rebasing
O rebase reescreve o histórico de commits, oferecendo uma linha do tempo mais linear:

```bash
git rebase nome-da-branch
```

3. Resetar mudanças

```bash
git reset #desfaz commits,

#movendo o ponteiro do HEAD:

git reset --soft HEAD~1  # Mantém mudanças no staging
git reset --hard HEAD~1  # Desfaz totalmente as mudanças
```

4. Reverter um commit
Para desfazer um commit mantendo o histórico, use git revert:

```bash
git revert <hash-do-commit>
```

5. Cherry-pick
O cherry-pick permite aplicar um commit específico de outra branch na branch atual:

```bash
git cherry-pick <hash-do-commit>
```

## Resolvendo Conflitos
Conflitos de merge acontecem quando duas alterações afetam a mesma linha de código. O Git marcará os conflitos, e você precisará resolvê-los manualmente.
Edite os arquivos com conflitos para escolher as alterações que devem ser mantidas.
Após resolver os conflitos, adicione os arquivos resolvidos:

```bash
git add arquivo-resolvido.txt
```

Finalize o merge com um commit:

```bash
git commit
```

## Colaborando em Repositórios Remotos
1. Clonar um repositório existente
Para copiar um repositório remoto para o seu computador:

```bash
git clone https://github.com/usuario/repo.git
```

2. Atualizar seu repositório local (Pull)
O comando git pull baixa as alterações do repositório remoto e as mescla com sua branch atual:

```bash
git pull origin main
```

3. Enviar mudanças para o repositório remoto (Push)
Após fazer commits, envie suas alterações para o repositório remoto com:

```bash
git push origin main
```

Considerações Finais
Esse tutorial cobre as operações mais comuns e intermediárias que você usará no dia a dia com Git. Para mais informações, consulte a documentação oficial do Git [documentação oficial do Git](https://git-scm.com/).

Sinta-se à vontade para abrir uma issue ou enviar um pull request caso tenha sugestões ou melhorias para este tutorial!


Este `README.md` serve como um guia completo e explicativo, ajudando os usuários a aprender e dominar as funcionalidades básicas e intermediárias do Git.

![GIF animado de exemplo](https://i.gifer.com/1zno.gif)