# PLANO DE AULA — Consumo de APIs públicas

| | |
|---|---|
| **Escola** | Etec Bento Quirino — Campinas/SP |
| **Componente curricular** | Programação Web III (Desenvolvimento de Sistemas — Novotec Integrado) |
| **Professor(a)** | _________________________________ |
| **Turma / Série** | 3ª série do Ensino Médio Integrado ao Técnico |
| **Data** | 27/05/2026 |
| **Duração** | 20 minutos (aula demonstrativa) |
| **Tema** | Consumo de APIs públicas |

---

## 1. Objetivo geral
Compreender o que é uma API web e ser capaz de **consumir dados de uma API pública** em uma
aplicação front-end usando JavaScript, tratando a resposta e os possíveis erros.

## 2. Objetivos específicos
Ao final da aula, o aluno será capaz de:
- Explicar os conceitos de **API**, **requisição/resposta HTTP** e **endpoint**;
- Reconhecer o formato **JSON** como padrão de troca de dados;
- Utilizar a função **`fetch()`** com `async/await` para requisitar dados;
- **Tratar erros** de requisição (rede/dado inexistente) com `try/catch`;
- Exibir os dados recebidos na interface (DOM).

## 3. Conteúdos
- Conceito de API (Application Programming Interface) e API pública;
- Cliente × servidor; métodos HTTP (foco no **GET**);
- Formato **JSON**;
- `fetch()`, `Promise`, `async/await`;
- Tratamento de erros e boas práticas (feedback de carregamento, fallback).

## 4. Recursos didáticos
- Quadro branco / projetor;
- Página de demonstração interativa (`aulas/tema1-apis.html`) — código à esquerda, execução à direita;
- Exemplo real: **API ViaCEP** (`https://viacep.com.br`) — gratuita e sem chave de acesso.

## 5. Metodologia / desenvolvimento (20 min)

| Tempo | Etapa | O que o professor faz |
|---|---|---|
| **0–3 min** | **Introdução / contextualização** | Pergunta motivadora: "Quando um app de entrega mostra o endereço só com o CEP, de onde vêm esses dados?". Apresenta o tema e **verbaliza os objetivos da aula**. Define API com uma analogia (o garçom entre você e a cozinha). |
| **3–8 min** | **Conceito** | Explica cliente/servidor, requisição HTTP **GET**, endpoint e resposta em **JSON**. Mostra no quadro a estrutura de um JSON de endereço. |
| **8–16 min** | **Demonstração** | Abre a página da demo. Lê o código (`fetch` → `await` → `.json()` → exibe). Roda ao vivo buscando o CEP da Etec (13024-045). Mostra o `console.log` da resposta e o tratamento de erro (`try/catch`). |
| **16–20 min** | **Fechamento + avaliação** | Síntese dos passos (requisitar → tratar → exibir). Propõe o exercício de avaliação e responde dúvidas. |

## 6. Interação com a turma
- Antes do código: "O que vocês acham que a API devolve: o site inteiro ou só os dados?"
- Durante a demo: pede um CEP da turma para buscar ao vivo.

## 7. Avaliação (instrumentos)
- **Formativa / observação** durante a demonstração (participação e respostas).
- **Exercício prático proposto:** alterar a demo para consumir a **API de Pokémons (PokéAPI)** ou
  a **API do GitHub**, exibindo 3 campos do JSON na tela. Critérios: requisição correta, tratamento
  de erro presente e dados exibidos no DOM.

## 8. Referências
- MDN Web Docs — *Fetch API* e *Using promises*. https://developer.mozilla.org/pt-BR/
- Documentação ViaCEP. https://viacep.com.br
- FLANAGAN, D. *JavaScript: O Guia Definitivo*. 7. ed. O'Reilly/Novatec.
