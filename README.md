# 🩸 Otimizador de Doações de Sangue por Compatibilidade Rápida 

## 🧩 Problema para Resolver (Inovação)

No Brasil e em muitos países, **pacientes em filas de doação de sangue enfrentam longas esperas**, muitas vezes por falta de um sistema eficiente de triagem e cruzamento de dados. Sendo assim, o **otimizador de doação de sangue** surge como uma solução inovadora para:

- Otimizar a compatibilidade entre doadores e receptores
- Reduzir o tempo de espera em situações críticas
- Gerenciar urgência com justiça e transparência
- Fornecer uma ferramenta educacional sobre doação e estrutura de dados

---

## ❗ Qual a sua relevância?

- Milhares de vidas são perdidas por atrasos na compatibilidade de doações.
- Hospitais nem sempre têm sistemas inteligentes de ordenação.
- O projeto simula como um **algoritmo bem estruturado pode literalmente salvar vidas**.
- É uma aplicação realista e ética do uso de **listas, filas, pilhas, árvores e tabelas hash**.

---

## 🛠️ Roteiro para Resolver (Criação)

1. Levantamento das estruturas necessárias para representar:
   - Pacientes em espera
   - Doador e receptor por tipo sanguíneo
   - Urgência do caso
   - Cancelamentos e desfazimentos
2. Construção de um sistema de menu para interações:
   - Registrar doadores e pacientes
   - Verificar compatibilidades
   - Processar doações por ordem de urgência
   - Cancelar e restaurar doadores
3. Implementação da lógica de compatibilidade com base nos grupos sanguíneos.
4. Aplicação da fila de prioridade para ordenar atendimentos.

---

## 🧠 Estruturas Utilizadas

| Estrutura        | Uso Principal                                                 |
|------------------|---------------------------------------------------------------|
| `Hash Table`     | Mapeia tipo sanguíneo → lista de doadores disponíveis         |
| `Lista`          | Armazena todos os pacientes cadastrados                       |
| `Fila de Prioridade` (`PriorityQueue`) | Ordena os pacientes conforme urgência (1 = mais urgente) |
| `Pilha`          | Armazena doadores que foram cancelados (para possível reversão) |
| `Função de decisão (tipo árvore)` | Verifica se o tipo sanguíneo do doador é compatível com o do receptor |
| `Ordenação implícita` | O sistema prioriza automaticamente os pacientes mais urgentes |

---

## 🧪 Script – Implementação

O projeto está implementado em Python puro (sem frameworks externos), com execução via terminal. Abaixo estão os principais módulos:

- `registrar_doador(nome, tipo)` → Adiciona doador ao grupo sanguíneo correspondente
- `registrar_paciente(nome, tipo, urgencia)` → Insere paciente na lista e na fila de prioridade
- `processar_doacoes()` → Busca compatibilidades e realiza as doações na ordem correta
- `cancelar_doador(nome)` → Remove doador e armazena na pilha de cancelados
- `desfazer_cancelamento()` → Reverte o cancelamento anterior
- `menu()` → Interface principal com o usuário
