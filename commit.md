# Commit

No contexto do Git, um **commit** é um registro permanente de alterações feitas em arquivos de um projeto.
Ele funciona como um “checkpoint” do código: você salva o estado atual do projeto junto com uma mensagem explicando o que mudou.

## O que um commit contém

Cada commit guarda:

* As alterações realizadas nos arquivos
* Um identificador único (hash)
* Autor da alteração
* Data e hora
* Mensagem descritiva

Exemplo de mensagem:

```bash
git commit -m "Corrige validação do login"
```

---

## Fluxo básico de commits

### 1. Modificar arquivos

Você altera arquivos do projeto normalmente.

---

### 2. Adicionar ao staging

O staging é uma área temporária onde você escolhe o que fará parte do commit.

```bash
git add arquivo.js
```

Ou tudo:

```bash
git add .
```

---

### 3. Criar o commit

```bash
git commit -m "Adiciona autenticação JWT"
```

---

## Estrutura de um commit

Um commit pode ser visto como:

```text
Commit
 ├── Hash único
 ├── Autor
 ├── Data
 ├── Mensagem
 └── Snapshot dos arquivos
```

O hash costuma parecer algo assim:

```text
a3f5c91d2b7e8...
```

---

## Por que commits são importantes

### Histórico do projeto

Você consegue ver tudo que foi alterado ao longo do tempo.

```bash
git log
```

---

### Reversão de erros

Se algo quebrar, é possível voltar para um commit anterior.

```bash
git checkout <hash>
```

ou

```bash
git revert <hash>
```

---

### Trabalho em equipe

Commits permitem que várias pessoas trabalhem no mesmo projeto sem perder alterações.

---

### Organização

Mensagens bem escritas ajudam a entender rapidamente o que mudou.

---

## Boas práticas para commits

### Faça commits pequenos

Melhor:

```text
Corrige cálculo do imposto
```

Pior:

```text
Várias mudanças
```

---

### Use mensagens claras

Padrões comuns:

```text
Adiciona funcionalidade X
Corrige erro Y
Remove código obsoleto
Refatora módulo Z
```

---

### Commits atômicos

Cada commit deve representar uma única mudança lógica.

---

## Tipos comuns de commits

Muitas equipes usam convenções como:

| Tipo     | Exemplo                        |
| -------- | ------------------------------ |
| feat     | `feat: adiciona carrinho`      |
| fix      | `fix: corrige login`           |
| refactor | `refactor: simplifica serviço` |
| docs     | `docs: atualiza README`        |
| test     | `test: adiciona testes da API` |

Isso é conhecido como **Conventional Commits**.

---

## Comandos úteis relacionados

### Ver histórico resumido

```bash
git log --oneline
```

### Ver diferenças antes do commit

```bash
git diff
```

### Alterar último commit

```bash
git commit --amend
```

### Ver detalhes de um commit

```bash
git show <hash>
```

---

## Exemplo prático

Imagine este fluxo:

```bash
git add .
git commit -m "feat: adiciona tela de cadastro"
git push origin main
```

Isso significa:

1. Adicionou arquivos modificados
2. Criou um checkpoint
3. Enviou para o repositório remoto

---

## Relação entre commit e branches

Cada branch possui sua sequência de commits.

Exemplo:

```text
main
 ├── Commit A
 ├── Commit B
 └── Commit C

feature/login
 ├── Commit B
 ├── Commit C
 └── Commit D
```

Quando faz merge, os commits são integrados.

---

## Conceito importante: commit ≠ salvar arquivo

Salvar um arquivo no editor apenas grava localmente.
O commit registra oficialmente a mudança no histórico do Git.

---

## Resumindo

Um commit:

* Salva alterações no histórico do projeto
* Cria pontos de restauração
* Facilita colaboração
* Documenta evolução do código
* É a unidade básica de versionamento no Git

Se quiser, também posso explicar:

* diferença entre `commit`, `push` e `merge`
* como funciona o histórico interno do Git
* boas práticas profissionais de commits
* Conventional Commits em detalhes
* como desfazer commits
* fluxo Git para equipes
* exemplos reais de commits em projetos grandes
