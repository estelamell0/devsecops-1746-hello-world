1.# Configuração inicial do Git

## 1. Instalar o Git no Sistema Operacional

Escolha o comando correspondente ao seu sistema.

### Linux (Ubuntu/Debian)

```bash
sudo apt update && sudo apt install git -y
```

### macOS (via Homebrew)

```bash
brew install git
```

### Windows

Baixe o instalador oficial em `git-scm.com/download/win` e execute mantendo as opções padrão recomendadas.

Alternativamente, via terminal (PowerShell com Winget):

```powershell
winget install --id Git.Git -e --source winget
```

Para verificar se a instalação ocorreu com sucesso, abra o terminal e execute:

```bash
git --version
```

## 2. Configurar Identidade Global

Define o autor que aparecerá em todos os commits.

Substitua com seu nome completo e o mesmo e-mail cadastrado na plataforma do repositório (GitHub, GitLab, etc.):

```bash
git config --global user.name "Seu Nome Completo"
git config --global user.email "seu-email@exemplo.com"
```

Defina também o nome padrão da branch principal para manter o alinhamento com os padrões modernos da indústria:

```bash
git config --global init.defaultBranch main
```

Valide as configurações salvas:

```bash
git config --list
```

## 3. Configurar Autenticação

Escolha entre HTTPS com Token ou Chave SSH.

### Opção 1: HTTPS (Recomendado para início rápido)

Plataformas como GitHub não aceitam mais senhas de conta no terminal. Ao fazer o primeiro push, utilize um Personal Access Token (Classic) gerado nas configurações da conta (`Settings > Developer Settings > Personal access tokens`) com o escopo `repo` marcado.

### Opção 2: Chave SSH (Padrão mais seguro em DevSecOps)

Gere uma chave Ed25519:

```bash
ssh-keygen -t ed25519 -C "seu-email@exemplo.com"
```

Pressione Enter para aceitar os caminhos padrão. Em seguida, exiba e copie a chave pública gerada:

```bash
cat ~/.ssh/id_ed25519.pub
```

Cole essa chave nas configurações de SSH da sua conta no GitHub/GitLab (`Settings > SSH and GPG keys`).

## 4. Clonar o Repositório e Acessar o Diretório

Copie a URL do repositório do curso e execute o comando correspondente ao método de autenticação escolhido:

### Via HTTPS

```bash
git clone git@github.com:estelamell0/devsecops-1746-hello-world.git
```

### Via SSH

```bash
git clone git@github.com:estelamell0/devsecops-1746-hello-world.git
```

Entre no diretório clonado para começar a atividade:

```bash
cd devsecops-onboarding
```
