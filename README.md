# Евгений Гладун — Frontend / Fullstack-разработчик

**Vue 3 · Nuxt · TypeScript · Node.js** — Екатеринбург · удалённо или гибрид

У меня больше 2 лет коммерческой разработки. В финтех-команде я работал над 6 фронтенд-приложениями и сделал там больше 1 000 коммитов. В одиночку переписал с нуля билетную платформу, от схемы БД до продакшена.

Мне важны понятная архитектура, строгая типизация и интерфейсы, которые быстро работают на телефоне.

[![Email](https://img.shields.io/badge/me@eev9enn.ru-0f172a?style=flat-square&logo=maildotru&logoColor=white)](mailto:me@eev9enn.ru)
[![Telegram](https://img.shields.io/badge/@EEv9ENN-0f172a?style=flat-square&logo=telegram&logoColor=27A0D9)](https://t.me/EEv9ENN)

---

## Опыт

### Fullstack-разработчик — [kassa-ugra.ru](https://kassa-ugra.ru/) · 2024 — сейчас

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

Код с работы закрыт NDA, поэтому основные подходы я заново реализовал в отдельном демо-проекте.

### [Live_Investment](https://github.com/EvgeniiGladun/Live_Investment) — кабинет инвестора и админка

`Vue 3` `TypeScript` `Pinia` `TanStack Query` `Zod` `Vitest`

| Что показывает | Где смотреть |
| --- | --- |
| Админ-панель: таблица с поиском, фильтрами, сортировкой, массовыми действиями, экспортом в CSV и состоянием в URL | `src/pages/admin/UsersPage.vue` |
| Личный кабинет: портфель с вкладками по статусам и выделением просрочек | `src/pages/PortfolioPage.vue` |
| Формы по JSON-схеме: поля появляются в зависимости от ответов, ошибки бэкенда показываются под полями | `src/modules/dynamic-form` |
| Авторизация: OTP, refresh-токены, доступ по ролям | `src/router`, `src/stores` |
| Адаптивность: на мобильном таблицы превращаются в карточки, есть бургер-меню | `src/modules/data-table` |

98 тестов. Бизнес-логика вынесена в чистые функции и покрыта unit-тестами.

---

## Стек

**Frontend**<br>
![Vue.js](https://img.shields.io/badge/Vue_3-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![Nuxt](https://img.shields.io/badge/Nuxt-00DC82?style=flat-square&logo=nuxt&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Pinia](https://img.shields.io/badge/Pinia-FFD859?style=flat-square&logo=pinia&logoColor=black)
![TanStack Query](https://img.shields.io/badge/TanStack_Query-FF4154?style=flat-square&logo=reactquery&logoColor=white)
![Zod](https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![SCSS](https://img.shields.io/badge/SCSS-CC6699?style=flat-square&logo=sass&logoColor=white)

**Backend**<br>
![Node.js](https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

**Инструменты**<br>
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![PM2](https://img.shields.io/badge/PM2-2B037A?style=flat-square&logo=pm2&logoColor=white)

---

<details>
<summary><b>Учебные проекты (Яндекс Практикум, 2023)</b></summary>
<br>

- [Movies Explorer](https://github.com/EvgeniiGladun/movies-explorer-frontend) — дипломный проект на React: поиск фильмов с фильтрами и сохранением в профиль.
- [Mesto](https://evgeniigladun.github.io/mesto) — галерея карточек с лайками и работой с API.
- [Путешествие по России](https://evgeniigladun.github.io/russian-travel/) — адаптивная вёрстка по БЭМ.
- [Виселица](https://evgeniigladun.github.io/game-Hangman/) — игра на чистом JavaScript.

</details>
