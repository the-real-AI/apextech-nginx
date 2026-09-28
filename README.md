# ApexTech — Nginx Multi-Port Web Platform

Полнофункциональная веб-платформа с двухпортовой архитектурой на базе Nginx.

## 🌐 Архитектура портов

- **Порт 80 (`http://localhost` или `http://akram.local`)**:
  - Главный Landing Page (`html/index.html`)
  - Демо-доступ (`html/try-demo.html`)
  - Регистрация аккаунтов (`html/register-account.html`)
  - Тарифные планы («Старт», «Про») и онлайн-покупка
  - Документация (`html/docs.html`)
  - Блог и статьи (`html/blog.html`)
  - Обратная связь (`html/contact.html`)
  - Кастомная страница 404 ошибки (`html/404.html`)

- **Порт 8080 (`http://localhost:8080` или `http://akram.local:8080`)**:
  - Административная панель управления / Dashboard (`html/panel/index.html`)
  - Живой лог Nginx и мониторинг трафика
  - Мониторинг загрузки ресурсов (CPU / RAM / Диск)
  - Таблица виртуальных хостов
  - Управление тарифами и быстрые действия

---

## 📂 Структура проекта

```text
├── conf/
│   └── nginx.conf              # Конфигурация Nginx с настройкой портов 80 и 8080
├── html/
│   ├── index.html              # Главная страница (Landing page)
│   ├── about.html              # О платформе
│   ├── try-demo.html           # Интерактивная демо-консоль
│   ├── register-account.html   # Регистрация пользователя
│   ├── plan-start.html         # Тариф «Старт»
│   ├── plan-pro.html           # Тариф «Про»
│   ├── contact.html            # Контакты поддержки
│   ├── docs.html               # Документация Nginx & API
│   ├── blog.html               # Блог и новости
│   ├── 404.html                # Кастомный экран 404 ошибки
│   ├── 50x.html                # Экран серверных ошибок
│   └── panel/
│       ├── index.html          # Дашборд / Панель управления (:8080)
│       └── 404.html            # 404 ошибка для панели
├── .gitignore
└── README.md
```

---

## 🚀 Установка и запуск

1. Склонируйте репозиторий или скопируйте файлы в папку Nginx:
   - Файлы из `html/` поместите в `C:\nginx\html\`
   - Файл `conf/nginx.conf` поместите в `C:\nginx\conf\nginx.conf`
2. Настройте домен `akram.local` в файле `C:\Windows\System32\drivers\etc\hosts`:
   ```text
   127.0.0.1 akram.local
   192.168.60.38 akram.local
   ```
3. Проверьте конфигурацию:
   ```cmd
   cd C:\nginx
   nginx.exe -t
   ```
4. Запустите Nginx:
   ```cmd
   nginx.exe
   ```
5. Для перезагрузки без остановки:
   ```cmd
   nginx.exe -s reload
   ```
