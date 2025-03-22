# go-web-template
Масштабируемый шаблон для веб-приложений на Golang

myapp/
├── cmd/                  # Главная точка входа (main.go)
│   ├── api/              # Запуск HTTP API
│   │   ├── main.go
│   │   ├── config.go
│   │   ├── wire.go       # DI (если используем wire)
│   │   └── logger.go     # Логгер
│   └── worker/           # Фоновая обработка (если нужна)
│       ├── main.go
│       └── jobs.go
├── config/               # Конфигурации (YAML, JSON, ENV)
│   ├── config.yaml
│   ├── config_test.yaml
│   ├── env.go
│   ├── env.example
│   └── loader.go
├── internal/             # Логика, которая не должна быть доступна извне
│   ├── app/              # Бизнес-логика
│   │   ├── service/      # Сервисы (use-cases)
│   │   ├── repository/   # Репозитории (работа с БД)
│   │   ├── entity/       # Сущности (модели данных)
│   │   └── dto/          # Data Transfer Objects
│   ├── transport/        # HTTP и gRPC слои
│   ├── infra/            # Инфраструктура (БД, кэш, брокеры)
│   ├── utils/            # Вспомогательные функции
├── migrations/           # SQL миграции
├── test/                 # Интеграционные тесты
├── docs/                 # Документация (Swagger, OpenAPI)
├── web/                  # Фронтенд (если нужен, например, Vue, React)
├── scripts/              # Скрипты деплоя и запуска
├── .gitignore
├── go.mod
├── go.sum
└── README.md
