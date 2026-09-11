# O teu ecossistema de IA

**Para:** quem dirige · **Julho de 2026**

Não é um pacote de ferramentas. É uma oficina.

A diferença aparece no dia em que precisares de um agente que não existe: em vez de o pedires a alguém,
descreves o que queres numa frase e o Cérebro constrói o, entrevista te, pontua o, e explica te as
decisões que tomou.

**Este repositório não traz agentes feitos de propósito.** Um agente que eu adivinhei é um agente que usas
duas vezes. O que falta para os construir bem é como tu trabalhas, e isso extrai se de ti, não se
supõe.

---

## Arranque, cerca de dez minutos

### 1. Instalar o Claude Code

```bash
npm install -g @anthropic-ai/claude-code
claude --version
```

Precisas de Node 18 ou superior e de uma conta Claude. Documentação: https://docs.claude.com/claude-code

### 2. Abrir esta pasta

```bash
cd ecossistema-claude-ceo
claude
```

### 3. Instalar os comandos

```bash
./scripts/instalar.sh
```

Ficas com `/cerebro` e dezassete ferramentas de ofício. Se já tiveres um comando com o mesmo nome, o
antigo é guardado numa cópia antes de ser substituído, e o instalador diz onde.

### 4. Deixar que ele te entreviste

```
claude
/cerebro entrevista
```

Ele faz te as perguntas uma a uma, quem és, do que respondes, o que nunca pode fazer por ti, e
preenche o teu contexto com as tuas palavras. No fim lê te o retrato de volta e corriges o que
estiver errado.

**Dez minutos aqui valem mais do que tudo o resto neste repositório.** É o que faz a diferença entre
um assistente genérico e um que sabe o que nunca deve fazer contigo.

Preferes à mão? `cp CLAUDE.md.template CLAUDE.md` e substitui os `[A PREENCHER]` nele e no
`cerebro/memory/core.md`.

### 5. Primeira pergunta a sério

```
/cerebro
```

Faz lhe uma pergunta real de trabalho, não um teste. Ele responde e diz te numa linha qual dos oito
modos escolheu. Se escolheu mal, dizes lhe, e essa correcção vai para a memória.

---

## O que está aqui

| Pasta | O que contém |
|---|---|
| `cerebro/` | O agente principal. Oito modos: o zero entrevista-te, o segundo é a Oficina que constrói os outros |
| `metodo/` | Nove documentos: anatomia, memória, SPAR, autonomia, orquestração, loops, qualidade, custo, erros |
| `seguranca/` | Cinco documentos e uma checklist. Segredos, repositórios de fora, injecção de prompt, permissões, dados pessoais |
| `skills/` | Dezassete ferramentas de ofício: gates de qualidade, design, memória, pensamento |
| `fichas/` | Três desenhos de agentes à espera da Oficina, e um catálogo de exemplos reais |
| `templates/` `scripts/` | Moldes e o instalador |
| `agentes/` | Vazia. É aqui que vão viver os que tu criares |

A pasta `agentes/` estar vazia é o ponto de partida, não uma omissão.

---

## Os oito modos do Cérebro

| Modo | Para quê |
|---|---|
| 0 · **Arranque** | Entrevista-te e preenche o teu contexto por ti. Corre no dia um, repete-se quando a realidade mudar |
| 1 · Pergunta | Responde do método citando a fonte. Sem fonte, diz que não sabe |
| 2 · **Oficina** | "preciso de um agente que..." e ele constrói o, pontua o, instala o, e ensina te |
| 3 · Afina | Melhora um agente que já tens, com pontuação antes e depois |
| 4 · **Calibra** | Melhora o teu Claude Code: regras, comandos, acessos, hooks, custo |
| 5 · Orquestra | Objectivos com vários passos, com plano e verificação |
| 6 · Loop | O resultado chega sem tu pedires |
| 7 · Memória | O contexto não morre entre sessões |

Os modos 2 e 4 são a razão de ser disto: um constrói os agentes, o outro melhora o ambiente onde
eles correm.

---

## As duas regras que não deves mudar

**Nenhum agente escreve em produção.** Lêem, analisam, propõem. A escrita fica do lado de quem
opera. Não é limitação técnica, é desenho: reduz o risco a quase zero e devolve te resposta em vez
de execução.

**Nada sai sem passar pelos gates.** Um número sem origem, um nome não confirmado, um texto que soa
a máquina. Quem assina és tu, portanto o custo do erro é teu.

---

## Quando algo não funcionar

Pergunta lhe directamente: *"porque é que fizeste assim"* ou *"o que precisas para isto funcionar"*.
Se faltar um acesso, ele diz qual em vez de inventar o resultado.

---

## Ler a seguir

**[COMECAR-AQUI.md](COMECAR-AQUI.md)**, uma página, com o dia 1, o dia 7 e o dia 30.
