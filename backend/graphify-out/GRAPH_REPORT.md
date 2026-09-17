# Graph Report - backend  (2026-09-17)

## Corpus Check
- Corpus is ~19,027 words - fits in a single context window. You may not need a graph.

## Summary
- 217 nodes · 378 edges · 9 communities (7 shown, 2 thin omitted)
- Extraction: 86% EXTRACTED · 13% INFERRED · 1% AMBIGUOUS · INFERRED: 49 edges (avg confidence: 0.85)
- Token cost: 313,928 input · 0 output

## Community Hubs (Navigation)
- Memory Data Model & Events
- Product Logic: Profile & Knowledge
- Six-Layer Backend Architecture
- Infrastructure, Deploy & Contracts
- UI Design & Graceful Degradation
- Tutor, Observer & Replay
- Preparation Route & Sets
- Fonts & Typography
- Versioned Prompts & Context

## God Nodes (most connected - your core abstractions)
1. `Evidence (свидетельство)` - 13 edges
2. `Наблюдатель (фоновое извлечение из чата)` - 10 edges
3. `TaskTemplate (шаблон задачи)` - 9 edges
4. `Обработка task.answered (правило, одна транзакция)` - 9 edges
5. `Слоты контекста топика` - 9 edges
6. `Сеты (построение маршрута и вкладка)` - 9 edges
7. `KnowledgeState (состояние навыка)` - 8 edges
8. `Подборка программ` - 8 edges
9. `L3 — ИИ / языковая модель` - 8 edges
10. `Лог событий events (append-only)` - 7 edges

## Surprising Connections (you probably didn't know these)
- `Набор инструментов модели (get_exam_format … get_skill_state)` --semantically_similar_to--> `Инструменты агентов как Python-функции с реестром`  [INFERRED] [semantically similar]
  README.md → ssot/tech-stack.md
- `Детерминированные правила (backend)` --references--> `L4 — Детерминированные правила`  [EXTRACTED]
  README.md → ssot/arch-logic.md
- `Ожидания фронтенда от бэкенда (контракт API)` --conceptually_related_to--> `Панель «Как я тебя вижу»`  [INFERRED]
  README.md → ssot/DESIGN.md
- `Ожидания фронтенда от бэкенда (контракт API)` --conceptually_related_to--> `Генерация типов из OpenAPI как контракт фронт↔бэк`  [INFERRED]
  README.md → ssot/tech-stack.md
- `Изоляция backend/ (свои конфиги, .env.example, секреты вне репозитория)` --conceptually_related_to--> `Монорепо quack/ (apps/web, apps/api, data, scripts, deploy, docs)`  [INFERRED]
  README.md → ssot/tech-stack.md

## Hyperedges (group relationships)
- **Поток извлечения знаний из чата (L → событие → R)** — ssot_memory_architecture_quack_observer, ssot_memory_architecture_quack_observer_output, ssot_memory_architecture_quack_events, ssot_memory_architecture_quack_evidence, ssot_memory_architecture_quack_knowledge_state, ssot_memory_architecture_quack_misconception_state [EXTRACTED 1.00]
- **Многослойные страховки от ложного наблюдения** — ssot_memory_architecture_quack_false_observation_risk, ssot_memory_architecture_quack_trust_tiers, ssot_memory_architecture_quack_misconception_statuses, ssot_memory_architecture_quack_misconception_visibility, ssot_memory_architecture_quack_provenance, ssot_memory_architecture_quack_replay [EXTRACTED 1.00]
- **Сборка контекста репетитора** — ssot_memory_architecture_quack_topic_context, ssot_memory_architecture_quack_session_line, ssot_memory_architecture_quack_context_slots, ssot_memory_architecture_quack_injection_format, ssot_memory_architecture_quack_policy, ssot_memory_architecture_quack_tutor_tools, ssot_memory_architecture_quack_tutor [EXTRACTED 1.00]
- **Пять принципов, на которых держится продукт** — ssot_product_logic_dva_istochnika_pravdy, ssot_product_logic_nikakoy_lishney_discipliny, ssot_product_logic_sistema_rekomenduet_uchenik_reshaet, ssot_product_logic_ii_na_vhode_i_vyhode, ssot_product_logic_nichego_bez_dokazatelstva [EXTRACTED 1.00]
- **Цепочка вывода: сохранённые → требования → вехи → маршрут → сет** — ssot_product_logic_sohranennye, ssot_product_logic_trebovanie, ssot_product_logic_veha, ssot_product_logic_marshrut, ssot_product_logic_set, ssot_product_logic_prognoznyy_ball [EXTRACTED 1.00]
- **Пайплайн датасета задач и моков** — ssot_product_logic_examformat, ssot_product_logic_shema_zadachi, ssot_product_logic_invarianty_datasseta, ssot_product_logic_sborka_mokov, ssot_product_logic_pul_zadach, ssot_product_logic_biblioteka_zabluzhdeniy [EXTRACTED 1.00]
- **Шестислойная архитектура Quack (L1–L6)** — ssot_arch_logic_l1_client, ssot_arch_logic_l2_orchestration, ssot_arch_logic_l3_ai, ssot_arch_logic_l4_deterministic_rules, ssot_arch_logic_l5_data, ssot_arch_logic_l6_external_sources [EXTRACTED 1.00]
- **Изоляция модели от записи: правило §7 → инструменты → правила → постпроверка** — ssot_arch_logic_rule_7, ssot_arch_logic_model_tools, ssot_tech_stack_agent_tools, ssot_tech_stack_output_postcheck, ssot_arch_logic_l4_deterministic_rules [INFERRED 0.95]
- **Поток деградации при отказе ИИ-слоя** — ssot_arch_logic_layer_degradation, ssot_arch_logic_fallback_controller, ssot_tech_stack_llm_status_fallback, ssot_arch_logic_text_generator, ssot_arch_logic_program_cache, ssot_design_honest_data [INFERRED 0.85]

## Communities (9 total, 2 thin omitted)

### Community 0 - "Memory Data Model & Events"
Cohesion: 0.09
Nodes (47): База знаний о поступлении и ExamFormat, Канонический слой графа, Канонизация заблуждений по эмбеддингу, Confidence (уверенность оценки), Конфиг (все параметры в одном месте), Перенос между экзаменами (transfer_cross_exam), Отказы и деградация, Замер (диагностика с очередью спуска) (+39 more)

### Community 1 - "Product Logic: Profile & Knowledge"
Cohesion: 0.08
Nodes (43): Анкета (структурированный слой профиля), Ассистент (единая языковая модель обоих разделов), База знаний о поступлении (GraphRAG), Библиотека заблуждений, Чат подбора, Чат подготовки (репетитор), Черты (неструктурируемые предпочтения), Принцип: два источника правды (+35 more)

### Community 2 - "Six-Layer Backend Architecture"
Cohesion: 0.07
Nodes (41): ИИ-слой backend (понимает и объясняет), API / оркестрация (backend entry point), Данные backend (профиль, программы, чаты, знания), Детерминированные правила (backend), Набор инструментов модели (get_exam_format … get_skill_state), Очередь фоновых задач (L2), Наблюдатель за чатом, Свидетельства → состояние навыков (+33 more)

### Community 3 - "Infrastructure, Deploy & Contracts"
Cohesion: 0.09
Nodes (23): Изоляция backend/ (свои конфиги, .env.example, секреты вне репозитория), Ожидания фронтенда от бэкенда (контракт API), Граф знаний о поступлении, Каноническая карта навыков, Модель знаний ученика (персональный слой), Ассистент «Подбор», Сборщик и подсчёт моков, Требования, вехи и конфликты (+15 more)

### Community 4 - "UI Design & Graceful Degradation"
Cohesion: 0.10
Nodes (23): Фоллбек-контроллер, L1 — Клиент, Деградация по слоям (§6.3), Планировщик Quack, Генератор текста (резюме, объяснения, гайдлайны, отчёт), Доступность (aria-label, role=tab, role=separator, aria-live), Анимации и кривые (--ease, --ease-out), Чат — главная поверхность (+15 more)

### Community 5 - "Tutor, Observer & Replay"
Cohesion: 0.15
Nodes (21): Приложение А: соответствие с memory-architecture.md, Слоты контекста топика, Риск ложного наблюдения, Индексы и изоляция персонального слоя, Идемпотентность по event_id, Формат инъекции learner_model, Метрики качества (Brier, resolved, точность наблюдателя), Статусы и переходы заблуждения (+13 more)

### Community 6 - "Preparation Route & Sets"
Cohesion: 0.19
Nodes (17): Дни активности, Календари экзаменов, Конфликты дедлайнов, Маршрут (последовательность сетов), Навык (единица учёта знаний), Принцип: никакой лишней дисциплины, Обзор подготовки, Quack! — сервис подбора программ и подготовки к экзаменам (+9 more)

## Ambiguous Edges - Review These
- `PostgreSQL (лог, профиль, кэши, read-модели)` → `База знаний о поступлении и ExamFormat`  [AMBIGUOUS]
  ssot/memory-architecture-quack.md · relation: shares_data_with
- `KnowledgeState (состояние навыка)` → `Открытые вопросы`  [AMBIGUOUS]
  ssot/memory-architecture-quack.md · relation: references
- `Next.js 15 App Router + TypeScript + Tailwind + shadcn/ui` → `Раскладка, ресайз панелей и брейкпоинты`  [AMBIGUOUS]
  ssot/DESIGN.md · relation: conceptually_related_to
- `TanStack Query как единый слой read-моделей` → `Левая колонка (навигация, программы, чаты)`  [AMBIGUOUS]
  ssot/DESIGN.md · relation: shares_data_with

## Knowledge Gaps
- **17 isolated node(s):** `Индексы и изоляция персонального слоя`, `memory-architecture.md (исходный документ)`, `Данные backend (профиль, программы, чаты, знания)`, `Ассистент-репетитор`, `Требования, вехи и конфликты` (+12 more)
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 21 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)
- **2 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **What is the exact relationship between `PostgreSQL (лог, профиль, кэши, read-модели)` and `База знаний о поступлении и ExamFormat`?**
  _Edge tagged AMBIGUOUS (relation: shares_data_with) - confidence is low._
- **What is the exact relationship between `KnowledgeState (состояние навыка)` and `Открытые вопросы`?**
  _Edge tagged AMBIGUOUS (relation: references) - confidence is low._
- **What is the exact relationship between `Next.js 15 App Router + TypeScript + Tailwind + shadcn/ui` and `Раскладка, ресайз панелей и брейкпоинты`?**
  _Edge tagged AMBIGUOUS (relation: conceptually_related_to) - confidence is low._
- **What is the exact relationship between `TanStack Query как единый слой read-моделей` and `Левая колонка (навигация, программы, чаты)`?**
  _Edge tagged AMBIGUOUS (relation: shares_data_with) - confidence is low._
- **Why does `L3 — ИИ / языковая модель` connect `Six-Layer Backend Architecture` to `Infrastructure, Deploy & Contracts`, `UI Design & Graceful Degradation`?**
  _High betweenness centrality (0.054) - this node is a cross-community bridge._
- **Why does `L2 — Оркестрация / API` connect `Six-Layer Backend Architecture` to `UI Design & Graceful Degradation`?**
  _High betweenness centrality (0.045) - this node is a cross-community bridge._
- **Why does `L1 — Клиент` connect `UI Design & Graceful Degradation` to `Six-Layer Backend Architecture`?**
  _High betweenness centrality (0.034) - this node is a cross-community bridge._