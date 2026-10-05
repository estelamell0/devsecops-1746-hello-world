# 🚀 Onboarding DevSecOps: Commit Your Career

Boas-vindas à nossa primeira entrega técnica! Em DevSecOps, rastreabilidade, automação e clareza de comunicação começam no controle de versão.

Para que todos se conheçam de forma objetiva, ágil e prática, sua apresentação será feita por meio de um arquivo Markdown no formato **Profile as Code** e um commit padronizado usando **Conventional Commits**.

> 💡 **Primeira vez configurando o Git?**  
> Se você ainda não tem o Git instalado ou configurado na sua máquina, siga o nosso [Guia de Configuração e Clone (SETUP.md)](./SETUP.md) antes de prosseguir.

---

## 🛠️ Passo a Passo Prático

### 1. Criar uma nova branch

Nunca faça alterações diretamente na branch `main`. Crie uma branch de trabalho usando o padrão de feature:

```bash
git checkout -b profile/<nome-sobrenome>
```

### 2. Criar o arquivo a partir do template

Copie o template base localizado em `Template de Perfil (template.md)` e salve-o com o seu nome e sobrenome dentro da pasta `profiles/`. Não preencha o arquivo ainda.

```bash
# Exemplo via terminal:
cp profiles/template.md profiles/<nome-sobrenome>.md
```

### 3. Fazer o primeiro commit (Arquivo base)

Adicione o arquivo criado e realize o primeiro commit informando a criação do perfil:

```bash
git add profiles/<nome-sobrenome>.md
git commit -m "feat(profile): adição de perfil <nome-sobrenome>"
```

### 4. Preencher seu perfil

Abra o arquivo `profiles/<nome-sobrenome>.md` no seu editor e preencha os campos com suas informações profissionais de forma objetiva.

### 5. Fazer o segundo commit (Carreira e objetivos)

Adicione as alterações e realize o commit seguindo a convenção de carreira:

```bash
git add profiles/<nome-sobrenome>.md
git commit -m "feat(carreira): <cargo atual>; goal: <objetivo>; expect: <expectativas>"
```

---

## 🧾 Convenções de Commit, Push e Pull Request

### Commit

A mensagem de commit serve como rastreabilidade da entrega. O cabeçalho deve ser curto, direto e seguir o padrão **Conventional Commits**.

Padrão esperado para esta atividade:

#### Commit 1 (Criação do template em branco)

```text
feat(profile): adição de perfil <nome-sobrenome>
```

Exemplo:

```text
feat(profile): adição de perfil maria-silva
```

#### Commit 2 (Arquivo preenchido com trajetória)

```text
feat(carreira): <cargo atual>; goal: <objetivos>; expect: <expectativas>
```

Exemplo:

```text
feat(carreira): sysadmin e suporte N3; goal: entender automações de segurança em desenvolvimento e migrar para área de segurança; expect: aprender sobre segurança em todo o ciclo de vida do software
```

### Push

O comando de push envia os commits registrados localmente para o repositório remoto.

Como fazer:

Como é a primeira vez que você envia essa branch, defina o upstream remoto:

```bash
git push -u origin profile/<nome-sobrenome>
```

> Nos próximos envios dentro da mesma branch, basta executar `git push`.

### Pull Request (PR)

O Pull Request propõe a integração das suas alterações à branch principal (`main`), servindo como a validação final da entrega.

Como fazer:

1. Acesse o repositório na interface web (GitHub/GitLab).
2. Clique no alerta **Compare & pull request** que aparece logo após o push (ou vá até a aba **Pull Requests > New Pull Request**).
3. Verifique as branches:
   - `base: main`
   - `compare: profile/<nome-sobrenome>`
4. Defina o título do PR:

```text
feat(profile): onboarding <Nome Sobrenome>
```

No corpo do PR, confirme se ambos os commits estão listados e clique em **Create pull request**.

