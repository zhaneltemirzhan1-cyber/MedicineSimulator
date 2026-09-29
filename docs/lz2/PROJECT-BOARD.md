# Настройка GitHub Projects для MedSim

## Статусы

- `Backlog` — идея или работа вне текущей итерации;
- `Ready` — есть критерии приемки, размер и зависимости;
- `In Progress` — назначен исполнитель и создана ветка;
- `Review` — открыт pull request;
- `Clinical Review` — медицинский контент проверяется преподавателем;
- `Testing` — выполняются технические и пользовательские проверки;
- `Done` — выполнены критерии готовности;
- `Blocked` — указаны причина и следующий шаг.

## Типы задач

`Epic`, `Feature`, `User Story`, `Task`, `Bug`, `Research`, `Documentation`, `Clinical Content`.

## Поля

| Поле | Значения |
|---|---|
| Priority | P0 Critical, P1 High, P2 Medium, P3 Low |
| Component | Auth, Exercises, Clinical Content, AI, Voice, 3D, Progress, Admin, Database, Infrastructure, UX, Documentation |
| Size | XS, S, M, L, XL |
| Risk | Low, Medium, High |
| Iteration | Двухнедельные итерации |
| Clinical review | Not Required, Required, Approved, Changes Requested |
| Target date | Плановая дата |

## Представления

1. `Delivery board` — группировка по статусу.
2. `Backlog` — таблица с сортировкой по приоритету и размеру.
3. `Clinical review` — задачи, требующие проверки медицинского содержания.
4. `Roadmap` — группировка по Epic и целевым датам.
5. `Risks` — задачи с `Risk: High` или `Blocked`.

## Автоматизация

- новый issue получает `Backlog`;
- открытие pull request переводит связанную задачу в `Review`;
- после технического review медицинский контент переводится в `Clinical Review`;
- объединение pull request закрывает связанную задачу только после выполнения Definition of Done.

