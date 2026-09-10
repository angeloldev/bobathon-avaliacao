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
├── AGENTS.md           Contexto do repositório para o IBM Bob
├── contexto/           Caso de uso, critérios de avaliação e roteiro
├── projetos/           Entregas das equipes (somente leitura para o harness)
└── saida/              Fichas, ranking e resultado gerados pelo avaliador
```

### O que colocar em `projetos/`

Cada equipe entrega uma pasta (ou `.zip`) dentro de `projetos/`, com a estrutura:

```
projetos/
└── equipe_XY/
    ├── README.md       Obrigatório — explica a solução
    ├── evidencias/     Prints, logs, exportações do watsonx Orchestrate
    └── src/            Código-fonte, se houver (opcional)
```

> O que não estiver na pasta não existe para a avaliação. Evidências do uso do watsonx Orchestrate são especialmente importantes.

---

## Para a organização — como o harness funciona

O avaliador é o IBM Bob rodando no modo **🧑‍⚖️ Jurado Bob-a-thon**. Ele lê cada pasta em `projetos/`, pontua contra a rubrica em `contexto/02_criterios_avaliacao.md` e grava as fichas em `saida/`.

### Documentos de referência

| Arquivo | Conteúdo |
|---|---|
| `contexto/01_caso_de_uso.md` | O desafio: o que as equipes deveriam construir |
| `contexto/02_criterios_avaliacao.md` | A rubrica: critérios, pesos e faixas |
| `contexto/03_roteiro_referencia.md` | Resumo do teatro de abertura |

### Antes de rodar

- [ ] Confirmar se o recurso **`controls` (governança)** está habilitado na instância do watsonx Orchestrate. Se não estiver, os 4 pontos de governança do critério 2.B não podem ser cobrados.
- [ ] Preencher datas, local e contato em `contexto/01_caso_de_uso.md` e `contexto/02_criterios_avaliacao.md`.
- [ ] Confirmar Python 3 (`python3 --version`) para o script de consolidação.

### Como rodar

Abra o repositório no IBM Bob e selecione o modo **🧑‍⚖️ Jurado Bob-a-thon**.

**Avaliar uma equipe:**
```
Avalie o projeto em projetos/<slug> contra a rubrica oficial.
Grave a ficha em saida/fichas/.
```

**Avaliar todas as equipes em lote:**
```
Avalie todos os projetos em projetos/. Uma ficha por equipe, gravada antes
de passar à próxima, sem fork_context entre elas.
```

**Eleger o vencedor** (depois que todas as fichas existirem):
```
Consolide o ranking e eleja o vencedor.
```

ou via script:
```bash
python3 .bob/skills/consolidar-ranking-bobathon/scripts/consolidar.py
```

### O que é gerado em `saida/`

| Arquivo | Conteúdo |
|---|---|
| `saida/00-inventario.md` | O que cada equipe entregou |
| `saida/fichas/<slug>.md` | Ficha legível por equipe |
| `saida/vencedor.md` | Eleição com justificativa por critério |
| `saida/ranking.md` | Ranking ordenado |
| `saida/ranking.csv` | Planilha de notas |

---

*Dúvidas sobre o evento: fale com a organização da IBM.*
