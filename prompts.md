# Biblioteca de prompts

Pedidos que funcionam, guardados para reuso.

---

## Transformar o que foi vendido em plano de execução

**Atualizado em:** 27/08/2026
**Por que este é o pedido mais importante do projeto:** é exatamente o ponto onde a consultoria trava. A venda funciona, a entrega depende de mim, e o que liga uma coisa à outra é este momento — pegar o que foi combinado com o cliente e transformar em algo que alguém consiga executar.

### As três versões

**V1 — o pedido como sairia sem aula nenhuma**

```
me ajuda a montar o plano do projeto desse cliente novo
```

*O que veio:* um plano genérico de projeto de marketing — diagnóstico, planejamento, execução, mensuração. Serve para qualquer cliente e por isso não serve para nenhum. Não perguntou o que foi vendido, não perguntou o prazo, e principalmente: não gerou nada que outra pessoa conseguisse pegar e executar sem mim explicando.

**V2 — o briefing completo**

```
TAREFA
Transforme o que eu vendi para este cliente em um plano de execução.
Antes de montar, me faça as perguntas que faltam.

FORMATO
1. O que foi vendido, em uma frase.
2. Tarefas por semana, com o que é entregue no fim de cada uma.
3. O que depende do cliente para acontecer, e em que semana trava se
   ele não entregar.
4. O que precisa ser decidido na primeira reunião.

AMOSTRA
O plano precisa ser específico o bastante para outra pessoa executar
sem falar comigo. Se uma linha exigir que alguém me pergunte algo, ela
está incompleta.

LIMITE
Não invente escopo que eu não vendi.
Não use termo genérico de marketing sem dizer o que sai como entrega
concreta naquela semana.
```

*O que veio:* o plano por semana, e uma pergunta que eu não tinha feito — o que acontece com o cronograma quando o cliente não entrega o que prometeu. Isso é metade dos meus atrasos e eu nunca tinha colocado no plano.

**V3 — reescrita pela IA (meta-prompting)**

O pedido acima foi submetido à crítica: *"este é um pedido que eu vou usar toda semana. Critique como um revisor exigente: o que está ambíguo, o que falta, o que sobra? Depois reescreva na melhor versão possível."*

A crítica apontou três coisas: o pedido não dizia quem ia executar cada tarefa; não separava o que é entrega para o cliente do que é trabalho interno; e não produzia nada para a reunião semanal, que é onde o projeto de fato é conduzido.

### O pedido que funciona

```
PERSONA
Você é um gestor de projetos experiente, acostumado a entregar
projetos de marketing recorrentes. Antes de responder, leia contexto/
e problema.md.

TAREFA
Transforme o que eu vendi para este cliente em um plano de execução
que outra pessoa consiga conduzir sem falar comigo.

Antes de montar, me faça as perguntas que faltam para o plano ficar
executável. Não monte com buraco.

FORMATO
1. O que foi vendido, em uma frase, na linguagem do cliente.
2. Plano por semana. Para cada semana: o que é entregue, quem executa,
   e o que precisa estar pronto antes.
3. Separe o que é entrega visível para o cliente do que é trabalho
   interno que sustenta a entrega.
4. O que depende do cliente, com a semana em que o cronograma trava se
   ele não entregar.
5. Pauta da primeira reunião: o que precisa ser decidido, e a pergunta
   exata a ser feita em cada ponto.

LIMITE
Não invente escopo que eu não vendi. Se não souber o que foi
combinado, pergunte.
Não escreva tarefa que dependa de me perguntar algo — se depender,
o plano está incompleto e você deve me dizer o que falta.
Não use termo genérico de marketing. Toda linha diz o que sai como
entrega concreta.
Marque as tarefas que exigem decisão estratégica, porque essas eu
ainda preciso revisar antes de delegar.
```

### O que aprendi

**O limite que mais mudou a resposta foi "não escreva tarefa que dependa de me perguntar algo"** — é o teste que transforma um plano bonito em um plano que outra pessoa consegue executar, que é o objetivo inteiro do projeto.

Dois desdobramentos:

- **A V2 me fez ver o que eu nunca tinha colocado no plano:** o que acontece quando o cliente não entrega a parte dele. É metade dos meus atrasos e vivia fora do cronograma.
- **O meta-prompt achou a coisa mais óbvia que faltava:** o plano não produzia nada para a reunião semanal — e a reunião é onde o projeto é conduzido de verdade.
