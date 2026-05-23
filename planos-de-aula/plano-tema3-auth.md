# PLANO DE AULA — Autenticação e autorização

| | |
|---|---|
| **Escola** | Etec Bento Quirino — Campinas/SP |
| **Componente curricular** | Programação Web III (Desenvolvimento de Sistemas — Novotec Integrado) |
| **Professor(a)** | Carlos Henrique Rebollo |
| **Turma / Série** | 3ª série do Ensino Médio Integrado ao Técnico |
| **Data** | 27/05/2026 |
| **Duração** | 20 minutos (aula demonstrativa) |
| **Tema** | Técnicas adicionais para o desenvolvimento Web: Autenticação e autorização |

---

## 1. Objetivo geral
Diferenciar **autenticação** de **autorização** e compreender como uma aplicação web identifica o
usuário e controla o que ele pode acessar.

## 2. Objetivos específicos
Ao final da aula, o aluno será capaz de:
- Distinguir **autenticação** ("quem é você?") de **autorização** ("o que você pode fazer?");
- Explicar o fluxo de **login → emissão de token → acesso a recurso protegido**;
- Compreender o conceito de **token** (ex.: JWT) e de **papéis/permissões** (roles);
- Reconhecer **boas práticas de segurança** (nunca guardar senha em texto puro, usar HTTPS).

## 3. Conteúdos
- Conceitos de **autenticação** e **autorização** e sua diferença;
- Fluxo de login e **credenciais**;
- **Token** como "crachá" digital de acesso (introdução ao JWT);
- Controle de acesso por **papel (role)**: admin × aluno;
- Boas práticas: senhas com hash, HTTPS, expiração de token.

## 4. Recursos didáticos
- Quadro branco / projetor;
- Página de demonstração interativa (`aulas/tema3-auth.html`) — código à esquerda, execução à direita,
  simulando login, emissão de token e verificação de permissão.

## 5. Metodologia / desenvolvimento (20 min)

| Tempo | Etapa | O que o professor faz |
|---|---|---|
| **0–3 min** | **Introdução / contextualização** | Analogia do **evento/balada**: a portaria confere seu documento (**autenticação**); a pulseira VIP diz a quais áreas você pode entrar (**autorização**). Apresenta o tema e **verbaliza os objetivos**. |
| **3–8 min** | **Conceito** | Define autenticação × autorização. Explica o fluxo: o usuário envia credenciais → o servidor valida → emite um **token** → o token acompanha as próximas requisições. |
| **8–16 min** | **Demonstração** | Abre a demo. Mostra a função `autenticar()` (gera token) e `autorizar()` (verifica o papel). Faz login como **admin** (acesso ao painel) e como **aluno** (acesso negado), e com **senha errada** (falha de autenticação). |
| **16–20 min** | **Fechamento + avaliação** | Reforça boas práticas (hash de senha, HTTPS, expiração). Síntese: autenticar ≠ autorizar. Propõe o exercício de avaliação. |

## 6. Interação com a turma
- "Você entrou no sistema (autenticado) mas a página de notas do professor não abre. Isso é falha de autenticação ou de autorização?"
- Pergunta por que **não** se deve guardar a senha em texto puro no banco.

## 7. Avaliação (instrumentos)
- **Formativa / observação** durante a demonstração.
- **Exercício prático proposto:** adicionar um terceiro papel (ex.: `coordenador`) e uma regra que
  libere uma área só para `admin` **e** `coordenador`. Critério: a verificação de autorização por papel
  está correta e separada da autenticação.

## 8. Referências
- MDN Web Docs — *Authentication* e *Authorization*. https://developer.mozilla.org/pt-BR/
- JWT — Introdução. https://jwt.io/introduction
- OWASP — *Authentication Cheat Sheet*. https://cheatsheetseries.owasp.org/
