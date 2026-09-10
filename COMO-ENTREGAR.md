# Como entregar o seu projeto — Bob-a-thon BRB 2026

> Guia para as equipes. Se alguém do seu time mexe com Git, este documento é para essa pessoa. Caso não tenha, chame um instrutor da IBM.

---

## O que você vai entregar

Uma pasta compactada (`.zip`) com o conteúdo do projeto da sua equipe, adicionada a este repositório via terminal.

**Nome da pasta:** `equipe_XY` — substitua `XY` pelo número da sua equipe (ex.: `equipe_01`, `equipe_07`, `equipe_14`).

---

## Estrutura obrigatória da pasta

Antes de zipar, organize a pasta assim:

```
equipe_XY/
├── README.md          ← O que a solução faz, como funciona,
│                         onde o Bob e o Orchestrate foram usados,
│                         e quem é a equipe
├── evidencias/        ← Prints, exportações dos agentes, logs,
│                         link de vídeo curto — tudo que mostra
│                         que a solução funcionou
└── src/               ← Código-fonte, se houver (opcional)
```

> **O `README.md` é obrigatório.** O jurado é o próprio IBM Bob lendo o repositório — o que não estiver na pasta não existe para a avaliação.
> O uso do watsonx Orchestrate **precisa estar nas evidências**: print, exportação ou log dos agentes configurados.

---

## Passo a passo: do zero até o envio

### 1. Crie a pasta do seu projeto localmente

Crie uma pasta com o nome `equipe_XY` no seu computador e coloque dentro dela o `README.md`, a pasta `evidencias/` e a pasta `src/` (se tiver código).

```
equipe_XY/
├── README.md
├── evidencias/
│   ├── print-agente-orchestrate.png
│   └── ...
└── src/
    └── ...
```

---

### 2. Compacte a pasta em um arquivo `.zip`

**macOS / Linux — terminal:**

```bash
zip -r equipe_XY.zip equipe_XY/
```

**Windows — PowerShell:**

```powershell
Compress-Archive -Path equipe_XY -DestinationPath equipe_XY.zip
```

Isso gera o arquivo `equipe_XY.zip` na mesma pasta onde você rodou o comando.

---

### 3. Clone o repositório do Bob-a-thon (se ainda não tiver feito)

```bash
git clone <URL-DO-REPOSITORIO>
cd harness-bob-bobathon-brb
```

> Substitua `<URL-DO-REPOSITORIO>` pela URL que a organização forneceu.

---

### 4. Mova o arquivo `.zip` para dentro da pasta `projetos/`

---

### 5. Adicione, faça commit e envie

```bash
git add projetos/equipe_XY.zip
git commit -m "entrega equipe_XY"
git push
```

Pronto. A entrega está feita.

---

## Checklist antes de enviar

- [ ] A pasta se chama `equipe_XY` (com o número correto da equipe)
- [ ] O `README.md` está na raiz da pasta
- [ ] A pasta `evidencias/` tem pelo menos um print ou exportação do watsonx Orchestrate
- [ ] O `.zip` foi colocado em `projetos/`
- [ ] O `git push` finalizou sem erro

---
