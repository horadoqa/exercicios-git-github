# Trabalhando com COMMITS

## Listando os Commits

```bash
git log
```

Resultado:

```bash
commit 156fe0e32315db5faf6bcbc6e9fcb9ad58b0a96e (HEAD -> semaforo, origin/semaforo)
Author: Ricardo Fahham <rfahham@hotmail.com>
Date:   Sun Mar 23 08:09:40 2025 -0300

    Mudando de cor - GREEN

commit 581f718a29149ca5d056b3fd860324da85862161
Author: Ricardo Fahham <rfahham@hotmail.com>
Date:   Sun Mar 23 08:08:00 2025 -0300

    Mudando de cor - YELLOW

commit a1a32efac0c76ad8ff6b9a6f4245511bdd242abe
Author: Ricardo Fahham <rfahham@hotmail.com>
Date:   Sun Mar 23 08:05:25 2025 -0300

    criando semáforo - RED
```

ou

```bash
git log --oneline

156fe0e - GREEN
581f718 - YELLOW
a1a32ef - RED
```

## Acessando/Alternando código de um Commit

Com o hash do commit em mãos (exemplo: a1a32ef), você pode alternar para esse commit usando:

```bash
git checkout a1a32ef
git checkout 581f718
```

## Alternar de Volta para a Última Branch

Se você deseja voltar para a branch em que estava antes de fazer o checkout, basta usar o comando:

```bash
git checkout semaforo
```