# Graph Report - frontend  (2026-09-17)

## Corpus Check
- Corpus is ~11,033 words - fits in a single context window. You may not need a graph.

## Summary
- 190 nodes · 344 edges · 9 communities
- Extraction: 100% EXTRACTED · 0% INFERRED · 0% AMBIGUOUS · INFERRED: 1 edges (avg confidence: 0.85)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `4a283e67`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- Program Comparison UI
- Assistant Dialogue Planner
- Chat Messages & Profile Fields
- Root Layout & Fonts
- Home Page & Roadmap
- Next Config & Choice Entry
- TypeScript Compiler Config
- Package Dependencies
- Frontend README Overview

## God Nodes (most connected - your core abstractions)
1. `ChoiceApp()` - 20 edges
2. `compilerOptions` - 16 edges
3. `react` - 13 edges
4. `evaluate()` - 10 edges
5. `programById()` - 9 edges
6. `Quack! — frontend` - 8 edges
7. `Profile` - 7 edges
8. `planReply()` - 7 edges
9. `Icon()` - 6 edges
10. `compareRows()` - 6 edges

## Surprising Connections (you probably didn't know these)
- `placeholderFor()` --calls--> `showChat()`  [EXTRACTED]
  src/components/choice/assistant.ts → src/components/choice/ChoiceApp.tsx
- `ChoiceApp()` --calls--> `fieldValue()`  [EXTRACTED]
  src/components/choice/ChoiceApp.tsx → src/components/choice/assistant.ts
- `applyToProfile()` --calls--> `fieldValue()`  [EXTRACTED]
  src/components/choice/ChoiceApp.tsx → src/components/choice/assistant.ts
- `CompareView()` --calls--> `compareRows()`  [EXTRACTED]
  src/components/choice/CompareView.tsx → src/components/choice/programs.ts
- `CompareView()` --calls--> `compareSummary()`  [EXTRACTED]
  src/components/choice/CompareView.tsx → src/components/choice/programs.ts

## Import Cycles
- None detected.

## Communities (9 total, 0 thin omitted)

### Community 0 - "Program Comparison UI"
Cohesion: 0.11
Nodes (31): Profile, CompareViewProps, IconName, CompareRow, Evaluation, Factor, FactorStatus, Level (+23 more)

### Community 1 - "Assistant Dialogue Planner"
Cohesion: 0.14
Nodes (24): MissingKey, Reply, acknowledge(), extract(), nextMissing(), placeholderFor(), planReply(), readiness() (+16 more)

### Community 2 - "Chat Messages & Profile Fields"
Cohesion: 0.13
Nodes (20): FieldKey, ChatMessageProps, ChatMsg, ChatItem, LeftPanel, RightPanel, Session, CustomScrollbarProps (+12 more)

### Community 5 - "Root Layout & Fonts"
Cohesion: 0.11
Nodes (19): DuckProps, Flight, TransitionApi, Duck(), FlyingDucks(), rand(), TransitionProvider(), intelOneMono (+11 more)

### Community 6 - "Home Page & Roadmap"
Cohesion: 0.17
Nodes (13): TopbarProps, StepState, TransitionLinkProps, Topbar(), Roadmap(), SiteHeader(), TransitionLink(), usePageTransition() (+5 more)

### Community 22 - "Next Config & Choice Entry"
Cohesion: 0.29
Nodes (4): ChoiceRoot(), nextConfig, metadata, next

### Community 3 - "TypeScript Compiler Config"
Cohesion: 0.11
Nodes (18): compilerOptions, allowJs, esModuleInterop, incremental, isolatedModules, jsx, lib, module (+10 more)

### Community 4 - "Package Dependencies"
Cohesion: 0.09
Nodes (21): dependencies, next, react, react-dom, devDependencies, @types/node, @types/react, @types/react-dom (+13 more)

### Community 7 - "Frontend README Overview"
Cohesion: 0.22
Nodes (8): graphify, Quack! — frontend, Адаптивность, Запуск, Стек, Страницы, Структура, Что имитируется и где подключать бэкенд

## Knowledge Gaps
- **80 isolated node(s):** `CompareViewProps`, `CompareRow`, `Evaluation`, `Factor`, `FactorStatus` (+75 more)
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 92 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `react` connect `Home Page & Roadmap` to `Program Comparison UI`, `Chat Messages & Profile Fields`, `Package Dependencies`, `Root Layout & Fonts`, `Next Config & Choice Entry`?**
  _High betweenness centrality (0.325) - this node is a cross-community bridge._
- **Why does `ChoiceApp()` connect `Assistant Dialogue Planner` to `Chat Messages & Profile Fields`, `Next Config & Choice Entry`?**
  _High betweenness centrality (0.063) - this node is a cross-community bridge._
- **Why does `next` connect `Next Config & Choice Entry` to `Package Dependencies`, `Root Layout & Fonts`?**
  _High betweenness centrality (0.041) - this node is a cross-community bridge._
- **What connects `CompareViewProps`, `CompareRow`, `Evaluation` to the rest of the system?**
  _80 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Program Comparison UI` be split into smaller, more focused modules?**
  _Cohesion score 0.1111111111111111 - nodes in this community are weakly interconnected._
- **Should `Assistant Dialogue Planner` be split into smaller, more focused modules?**
  _Cohesion score 0.13675213675213677 - nodes in this community are weakly interconnected._
- **Should `Chat Messages & Profile Fields` be split into smaller, more focused modules?**
  _Cohesion score 0.13 - nodes in this community are weakly interconnected._