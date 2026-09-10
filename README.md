# Bob-a-thon BRB 2026

Bem-vindo ao repositório oficial do **Bob-a-thon BRB 2026**.

Aqui ficam as entregas das equipes e o sistema de avaliação do evento. A avaliação é feita automaticamente pelo **IBM Bob**, que lê os projetos e pontua cada equipe contra a rubrica oficial.

---

## Para as equipes — como entregar o projeto

👉 **[Leia o guia de entrega: COMO-ENTREGAR.md](COMO-ENTREGAR.md)**

O guia explica passo a passo como subir o projeto neste repositório, incluindo uma seção para quem nunca usou o terminal.

**Resumo rápido:**

1. Crie uma pasta chamada `equipe_XY` (substitua `XY` pelo número da sua equipe).
2. Coloque dentro dela o `README.md`, a pasta `evidencias/` e a pasta `src/` (se tiver código).
3. Compacte em um `.zip` e coloque dentro da pasta `projetos/` deste repositório.
4. Faça `git add`, `git commit` e `git push`.

Dúvida? Leia o [COMO-ENTREGAR.md](COMO-ENTREGAR.md) ou chame um instrutor da IBM.

---

## Estrutura do repositório

```
/
├── README.md           Este arquivo
├── COMO-ENTREGAR.md    Guia de entrega para as equipes
```

### O que colocar no repositório

Cada equipe entrega uma pasta (ou `.zip`) dentro da raiz do repositório, com a estrutura:

```
equipe_XY/
    ├── README.md       Obrigatório — explica a solução
    ├── evidencias/     Prints, logs, exportações do watsonx Orchestrate
    └── src/            Código-fonte, se houver (opcional)
```

> O que não estiver na pasta não existe para a avaliação. Evidências do uso do watsonx Orchestrate são especialmente importantes.


*Dúvidas sobre o evento: fale com a organização da IBM.*
