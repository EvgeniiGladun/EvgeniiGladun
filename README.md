# Евгений Гладун — Frontend / Fullstack-разработчик

**Vue 3 · Nuxt · TypeScript · Node.js** — Екатеринбург · удалённо или гибрид

У меня больше 2 лет коммерческой разработки. В финтех-команде я работал над 6 фронтенд-приложениями и сделал там больше 1 000 коммитов. В одиночку переписал с нуля билетную платформу, от схемы БД до продакшена.

Мне важны понятная архитектура, строгая типизация и интерфейсы, которые быстро работают на телефоне.

[![Email](https://img.shields.io/badge/me@eev9enn.ru-0f172a?style=flat-square&logo=maildotru&logoColor=white)](mailto:me@eev9enn.ru)
[![Telegram](https://img.shields.io/badge/@EEv9ENN-0f172a?style=flat-square&logo=telegram&logoColor=27A0D9)](https://t.me/EEv9ENN)

---

## Опыт

### Fullstack-разработчик — [kassa-ugra.ru](https://kassa-ugra.ru/) · 2024 — сейчас (проектная занятость)

Билетная афиша. Переписал её в одиночку: раньше она работала на PHP 7, jQuery и внешнем API, который собирались отключить. Теперь это мультигородская платформа, где у каждого города свой поддомен.

- **Архитектура:** Nuxt 4 (SSR) на фронтенде, Express + Prisma + PostgreSQL на бэкенде. Схему БД спроектировал сам.
- **Миграция без потерь:** логировал ответы старого API в JSONL, затем импортировал и дедуплицировал данные. Старый API сохранил ради обратной совместимости.
- **Интеграция с Яндекс.Билетами:** синхронизация каталога через upsert по `external_id`, журнал синхронизаций, запуск по cron.
- **CMS-админка:** JWT, 4 роли, CRUD-разделы, загрузка и обработка изображений (sharp).
- **SEO и PWA:** JSON-LD, динамические sitemap и robots, офлайн-режим.
- **Безопасность:** helmet, rate-limit, валидация входных данных через Zod.

### Frontend-разработчик (Vue 3 / TypeScript) — финтех-платформа для инвестиций · 2024 — 2026

Экосистема из 6 приложений: личный кабинет инвестора, CRM для сотрудников, сервис авторизации, внутренние сервисы и общий UI-kit.

- **Личный кабинет:** перевёл проект с JS на TypeScript и добавил проверку контрактов с API через Zod. Сделал анкеты на динамических формах, график возвратов (аннуитетный и отложенный) и SMS/OTP-подтверждение с guard'ом.
- **CRM:** универсальная таблица с фильтрами, пагинацией и экспортом. Сделал блокировку пользователей с историей, работу с платежами (защита от повторной оплаты, расчёт пени) и мультизагрузку документов.
- **Авторизация:** вход, регистрация, обновление токенов. Настроил генерацию API-клиента из Swagger: типы, Zod-схемы и хуки Vue Query создаются автоматически.
- **UI-kit:** вынес библиотеку в отдельную сборку и подключил её как npm-пакет. Сделал сервис модальных окон на Pinia, ввёл дизайн-токены и адаптировал компоненты под мобильные. Перевёл проект на Vite 8 / Rolldown.
- **В команде:** code review, стандарты кода, менторинг junior-разработчиков, согласование API с бэкендом, планирование спринтов.

---

## Пример кода

Код с работы закрыт NDA, поэтому основные подходы я заново реализовал в отдельном демо-проекте — на вымышленных данных и в другой предметной области.

### [TechRent](https://github.com/EvgeniiGladun/TechRent) — аренда спецтехники с правом выкупа: кабинет арендатора и админка

`Vue 3` `TypeScript` `Pinia` `TanStack Query` `Zod` `Vitest`

| Что показывает | Где смотреть |
| --- | --- |
| Админ-панель: таблица с поиском, фильтрами, сортировкой, массовыми действиями, экспортом в CSV и состоянием в URL | `src/pages/admin/UsersPage.vue` |
| Личный кабинет: аренды с вкладками по статусам, выделением просрочек и сводкой платежей | `src/pages/RentalsPage.vue` |
| Калькулятор аренды: лимиты по парку, залогу и годовому лимиту, график платежей (равные платежи или выкуп в конце срока) с расчётом в копейках | `src/modules/rent` |
| Формы по JSON-схеме: поля появляются в зависимости от ответов, ошибки бэкенда показываются под полями | `src/modules/dynamic-form` |
| Авторизация: OTP, refresh-токены, доступ по ролям | `src/router`, `src/stores` |
| Адаптивность: на мобильном таблицы превращаются в карточки, есть бургер-меню | `src/modules/data-table` |

98 тестов. Бизнес-логика вынесена в чистые функции и покрыта unit-тестами.

---

## Стек

Наведите на бейдж — появится краткое описание опыта, клик откроет подробности.

**Frontend**<br>
[![Vue 3](https://img.shields.io/badge/Vue_3-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)](./rsc/languagesAndTechnologies.md#vue-3 "Основной фреймворк 2+ года: 6 приложений финтех-платформы, generic-компоненты, динамические формы")
[![Nuxt](https://img.shields.io/badge/Nuxt-00DC82?style=flat-square&logo=nuxt&logoColor=white)](./rsc/languagesAndTechnologies.md#nuxt "Nuxt 4 SSR: мультигородская билетная платформа, SEO, JSON-LD, PWA")
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](./rsc/languagesAndTechnologies.md#typescript "Strict-режим. Перевёл кабинет инвестора с JS на TS, генерация API-клиента из Swagger")
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](./rsc/languagesAndTechnologies.md#javascript "ES2022+, асинхронность, браузерные API")
[![Pinia](https://img.shields.io/badge/Pinia-FFD859?style=flat-square&logo=pinia&logoColor=black)](./rsc/languagesAndTechnologies.md#pinia "Клиентское состояние, централизованный сервис модальных окон")
[![TanStack Query](https://img.shields.io/badge/TanStack_Query-FF4154?style=flat-square&logo=reactquery&logoColor=white)](./rsc/languagesAndTechnologies.md#tanstack-query "Кэш серверных данных, инвалидация, пагинация, защита от повторных платежей")
[![Zod](https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white)](./rsc/languagesAndTechnologies.md#zod "Проверка контрактов с API и валидация входных данных")
[![HTML / CSS](https://img.shields.io/badge/HTML_%2F_CSS-E34F26?style=flat-square&logo=html5&logoColor=white)](./rsc/languagesAndTechnologies.md#html--css "Адаптивная вёрстка, mobile-first, БЭМ, доступность")
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)](./rsc/languagesAndTechnologies.md#tailwind-css "Публичный сайт и админка билетной платформы")
[![SCSS](https://img.shields.io/badge/SCSS-CC6699?style=flat-square&logo=sass&logoColor=white)](./rsc/languagesAndTechnologies.md#scss "UI-kit: дизайн-токены, SVG-спрайт, адаптив компонентов")

**Backend**<br>
[![Node.js](https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white)](./rsc/languagesAndTechnologies.md#nodejs "Бэкенд, скрипты миграции данных, синхронизация по cron")
[![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)](./rsc/languagesAndTechnologies.md#express "JWT, 4 роли, helmet, rate-limit, загрузка изображений")
[![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)](./rsc/languagesAndTechnologies.md#prisma "Схема, миграции, upsert по external_id")
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](./rsc/languagesAndTechnologies.md#postgresql "Спроектировал схему БД билетной платформы")
[![REST API](https://img.shields.io/badge/REST_API-0f172a?style=flat-square&logo=openapiinitiative&logoColor=white)](./rsc/languagesAndTechnologies.md#rest-api "Проектирование эндпоинтов, обратная совместимость, согласование спецификаций")

**Инструменты**<br>
[![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)](./rsc/languagesAndTechnologies.md#vite "Изолированная сборка UI-kit, переход на Vite 8 / Rolldown")
[![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white)](./rsc/languagesAndTechnologies.md#vitest "Unit-тесты бизнес-логики и компонентов")
[![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)](./rsc/languagesAndTechnologies.md#git "1 000+ коммитов, feature-ветки, code review")
[![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)](./rsc/languagesAndTechnologies.md#nginx "Reverse proxy, поддомены, статика")
[![PM2](https://img.shields.io/badge/PM2-2B037A?style=flat-square&logo=pm2&logoColor=white)](./rsc/languagesAndTechnologies.md#pm2 "Запуск Node.js-приложений в продакшене")

---

<details>
<summary><b>Учебные проекты (Яндекс Практикум, 2023)</b></summary>
<br>

- [Movies Explorer](https://github.com/EvgeniiGladun/movies-explorer-frontend) — дипломный проект на React: поиск фильмов с фильтрами и сохранением в профиль.
- [Mesto](https://evgeniigladun.github.io/mesto) — галерея карточек с лайками и работой с API.
- [Путешествие по России](https://evgeniigladun.github.io/russian-travel/) — адаптивная вёрстка по БЭМ.
- [Виселица](https://evgeniigladun.github.io/game-Hangman/) — игра на чистом JavaScript.

</details>
