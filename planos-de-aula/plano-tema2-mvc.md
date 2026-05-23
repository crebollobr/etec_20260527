# PLANO DE AULA — Frameworks Model–View–Controller (MVC)

| | |
|---|---|
| **Escola** | Etec Bento Quirino — Campinas/SP |
| **Componente curricular** | Programação Web III (Desenvolvimento de Sistemas — Novotec Integrado) |
| **Professor(a)** | Carlos Henrique Rebollo |
| **Turma / Série** | 3ª série do Ensino Médio Integrado ao Técnico |
| **Data** | 27/05/2026 |
| **Duração** | 20 minutos (aula demonstrativa) |
| **Tema** | Utilização de frameworks Model–View–Controller (MVC) para o desenvolvimento Web |

---

## 1. Objetivo geral
Compreender o padrão de arquitetura **MVC** e como ele organiza uma aplicação web, **separando
responsabilidades** entre dados, apresentação e controle.

## 2. Objetivos específicos
Ao final da aula, o aluno será capaz de:
- Definir as três camadas: **Model** (dados/regras), **View** (interface) e **Controller** (controle/eventos);
- Explicar **por que** separar responsabilidades (manutenção, organização, trabalho em equipe);
- Identificar o fluxo de informação entre as camadas;
- Reconhecer o padrão em **frameworks reais** (Laravel, Spring, ASP.NET, Angular).

## 3. Conteúdos
- O problema do "código tudo misturado" (acoplamento);
- Padrão arquitetural **MVC** e o princípio da **separação de responsabilidades**;
- Papel de cada camada e o **fluxo**: usuário → Controller → Model → View → usuário;
- Relação com frameworks MVC do mercado.

## 4. Recursos didáticos
- Quadro branco / projetor;
- Página de demonstração interativa (`aulas/tema2-mvc.html`) — código (Model/View/Controller separados)
  à esquerda e o app rodando à direita;
- Diagrama do fluxo MVC no quadro.

## 5. Metodologia / desenvolvimento (20 min)

| Tempo | Etapa | O que o professor faz |
|---|---|---|
| **0–3 min** | **Introdução / contextualização** | Mostra (ou descreve) um código onde HTML, dados e lógica estão todos juntos e pergunta: "Se a tela mudar, o que mais quebra?". Apresenta o tema e **verbaliza os objetivos**. |
| **3–7 min** | **Conceito** | Desenha o diagrama MVC no quadro. Explica cada camada com a analogia do restaurante: **Model** = cozinha/estoque, **View** = prato servido, **Controller** = garçom. |
| **7–16 min** | **Demonstração** | Abre a demo. Percorre o código mostrando os 3 blocos separados (Model, View, Controller). Roda o app (lista de tarefas): adiciona e marca tarefas, mostrando que **só o Model guarda dados** e **só a View desenha**. |
| **16–20 min** | **Fechamento + avaliação** | Conecta com frameworks reais (Laravel/Spring/Angular). Síntese das vantagens. Propõe o exercício de avaliação. |

## 6. Interação com a turma
- "Se eu quiser trocar a aparência da lista sem mexer nas regras, qual camada eu altero?"
- Pede um exemplo de "dado" e um de "regra de negócio" para classificar como Model.

## 7. Avaliação (instrumentos)
- **Formativa / observação** durante a demonstração.
- **Exercício prático proposto:** adicionar ao app uma função "remover tarefa", indicando em **qual
  camada** vai cada parte (regra no Model, botão na View, evento no Controller). Critério: a separação
  de responsabilidades é respeitada.

## 8. Referências
- FOWLER, M. *Patterns of Enterprise Application Architecture*. Addison-Wesley.
- MDN Web Docs — *MVC*. https://developer.mozilla.org/pt-BR/docs/Glossary/MVC
- Documentação oficial do Laravel / Spring MVC / Angular.
