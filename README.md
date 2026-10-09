# 🚀 Onboarding DevSecOps: Commit Your Career

Boas-vindas à nossa primeira entrega técnica! Em DevSecOps, rastreabilidade, automação e clareza de comunicação começam no controle de versão.

Para que todos se conheçam de forma objetiva, ágil e prática, sua apresentação será feita por meio de um arquivo Markdown no formato **Profile as Code** e um commit padronizado usando **Conventional Commits**.

> 💡 **Primeira vez configurando o Git?**  
> Se você ainda não tem o Git instalado ou configurado na sua máquina, siga o nosso [Guia de Configuração e Clone (SETUP.md)](./SETUP.md) antes de prosseguir.

---

## 🛠️ Passo a Passo Prático

> **Identificador:** Nos comandos e arquivos abaixo, substitua `<identificador>` pelo seu formato preferido: `nome-sobrenome` (ex.: `maria-silva`) ou um hash curto/apelido (ex.: `a8f3b1`).

### 0. Fork e Clone do Repositório

1. Acesse o repositório principal: [https://github.com/estelamell0/devsecops-1746-hello-world](https://github.com/estelamell0/devsecops-1746-hello-world).
2. No canto superior direito da página, clique no botão **Fork** e depois em **Create fork** para criar uma cópia no seu próprio perfil do GitHub.
3. Clone o **seu fork** (substitua `SEU_USUARIO` pelo seu username do GitHub):

```bash
# Opção via SSH (recomendada se já tiver chaves configuradas):
git clone git@github.com:SEU_USUARIO/devsecops-1746-hello-world.git
```

```bash
# Opção via HTTPS:
git clone https://github.com/SEU_USUARIO/devsecops-1746-hello-world.git
```

4. Acesse a pasta do projeto clonado:

```bash
cd devsecops-1746-hello-world
```

---

### 1. Criar uma nova branch

Nunca faça alterações diretamente na branch `main`. Crie uma branch de trabalho usando o padrão de feature:

```bash
git checkout -b profile/<identificador>
```

```bash
# Exemplo:
git checkout -b profile/maria-silva
```

---

### 2. Criar o arquivo a partir do template

Copie o template base localizado em `profiles/template.md` e salve-o com o seu identificador dentro da pasta `profiles/`. 
Não preencha o arquivo ainda.

```bash
# Via terminal:
cp profiles/template.md profiles/<identificador>.md
```

```bash
# Exemplo:
cp profiles/template.md profiles/maria-silva.md
```

---

### 3. Fazer o primeiro commit (Arquivo base)

Adicione o arquivo criado e realize o primeiro commit informando a criação do perfil:

```bash
git add profiles/<identificador>.md
git commit -m "feat(profile): adição de perfil <identificador>"
```

```bash
# Exemplo:
git add profiles/maria-silva.md
git commit -m "feat(profile): adição de perfil maria-silva"
```

---

### 4. Preencher seu perfil

Abra o arquivo `profiles/<identificador>.md` no seu editor de código e preencha os campos com suas informações profissionais de forma objetiva.

---

### 5. Fazer o segundo commit (Carreira e objetivos)

Adicione as alterações e realize o commit seguindo a convenção de carreira:

```bash
git add profiles/<identificador>.md
git commit -m "feat(carreira): <cargo atual>; goal: <objetivo>; expect: <expectativas>"
```

```bash
# Exemplo:
git add profiles/maria-silva.md
git commit -m "feat(carreira): sysadmin e suporte N3; goal: entender automações de segurança em desenvolvimento e migrar para área de segurança; expect: aprender sobre segurança em todo o ciclo de vida do software"
```

---

### 6. Enviar as alterações (Push)

O comando de push envia os commits registrados localmente para o seu repositório remoto (seu fork no GitHub).

Como é a primeira vez que você envia essa branch, defina o upstream remoto:

```bash
git push -u origin profile/<identificador>
```

```bash
# Exemplo:
git push -u origin profile/maria-silva
```

> **Dica:** Nos próximos envios dentro dessa mesma branch, basta executar apenas `git push`.

---

### 7. Abrir o Pull Request (PR)

O Pull Request propõe a integração das suas alterações à branch principal do repositório upstream (original).

1. Acesse a página do seu fork no GitHub (`https://github.com/SEU_USUARIO/devsecops-1746-hello-world`).
2. Clique no botão amarelo **Compare & pull request** que aparece no topo da página logo após o push.
   * *Caso o banner não apareça:* vá na aba **Pull requests**, clique em **New pull request** e, se necessário, no link **compare across forks**.
3. Verifique o direcionamento das branches:
   * **base repository:** `estelamell0/devsecops-1746-hello-world` | **base:** `main`
   * **head repository:** `SEU_USUARIO/devsecops-1746-hello-world` | **compare:** `profile/<identificador>`
4. Defina o título do PR:

```text
feat(profile): onboarding <identificador>
```

5. Na descrição do PR, confirme se os dois commits estão listados na aba de commits e clique no botão verde **Create pull request**.