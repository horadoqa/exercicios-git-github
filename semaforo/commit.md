# Trabalhando com COMMITS

Neste exemplo `VISUAL`, você poderá entender como funciona a transição entre commits.

Acessar a Branch: `semaforo` 

```bash
git checkout semaforo
```

## Listando os Commits

```bash
git log
```

Resultado:

```bash
commit 6687ac04a2d99adc2705c1ed6bdb00d6a6e989a3 (HEAD -> semaforo, origin/semaforo)
Author: Ricardo Fahham <rfahham@hotmail.com>
Date:   Sun Mar 23 10:39:23 2025 -0300

    GREEN

commit 9042133181ace84fd8f861864499d4778b4594c4
Author: Ricardo Fahham <rfahham@hotmail.com>
Date:   Sun Mar 23 10:37:29 2025 -0300

    YELLOW

commit 61642bd67cbd6b225387c93f40d48162d9995c09
Merge: 7b0fc5a fc76b0f
Author: Hora do QA <horadoqa@gmail.com>
Date:   Sun Mar 23 10:20:56 2025 -0300

    Merge pull request #1 from horadoqa/semaforo
    
    Adicionando projeto semaforo
```

ou

```bash
git log --oneline

fc76b0f - RED
9042133 - YELLOW
6687ac0 - GREEN
```

## Acessando/Alternando código de um Commit

Com o hash do commit em mãos (exemplo: a1a32ef), você pode alternar para esse commit usando:

```bash
git checkout fc76b0f
git checkout 9042133
git checkout 6687ac0
```

## Alternar de Volta para a Última Branch

Se você deseja voltar para a branch em que estava antes de fazer o checkout, basta usar o comando:

```bash
git checkout semaforo
```