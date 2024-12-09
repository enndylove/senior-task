# Senior task

## How to create great project architecture? Feature-sliced architecture

#### Go to workdir(in us example is src folder)
```shell
cd src
```
#### Make architecture folders
```shell
mkdir -p processes/Main/lib 
mkdir -p processes/Main/model 
mkdir -p pages/Main/lib 
mkdir -p pages/Main/model 
mkdir -p pages/Main/ui} 
mkdir -p features/Main/lib 
mkdir -p features/Main/model 
mkdir -p features/Main/ui 
mkdir -p entities/Main/lib 
mkdir -p entities/Main/model 
mkdir -p entities/Main/ui 
mkdir -p shared/api 
mkdir -p shared/lib 
mkdir -p shared/ui 
```

#### Folders Doc - take of [wiki](https://github.com/julieobolenskaya/wiki?tab=readme-ov-file)
```text
└── src/
    ├── app/                    # Layer: Приложение
    |                           #
    ├── processes/              # Layer: Процессы (опционален)
    |   ├── {some-process}/     #     Slice: (н-р процесс CartPayment)
    |   |   ├── lib/            #         Segment: Инфраструктурная-логика (хелперы)
    |   |   └── model/          #         Segment: Бизнес-логика
    |   ...                     #
    |                           #
    ├── pages/                  # Layer: Страницы
    |   ├── {some-page}/        #     Slice: (н-р страница ProfilePage)
    |   |   ├── lib/            #         Segment: Инфраструктурная-логика (хелперы)
    |   |   ├── model/          #         Segment: Бизнес-логика
    |   |   └── ui/             #         Segment: UI-логика
    |   ...                     #
    |                           #
    ├── features/               # Layer: Фичи
    |   ├── {some-feature}/     #     Slice: (н-р фича AuthByPhone)
    |   |   ├── lib/            #         Segment: Инфраструктурная-логика (хелперы)
    |   |   ├── model/          #         Segment: Бизнес-логика
    |   |   └── ui/             #         Segment: UI-логика
    |   ...                     #
    |                           #
    ├── entities/               # Layer: Бизнес-сущности
    |   ├── {some-entity}/      #     Slice: (н-р сущность User)
    |   |   ├── lib/            #         Segment: Инфраструктурная-логика (хелперы)
    |   |   ├── model/          #         Segment: Бизнес-логика
    |   |   └── ui/             #         Segment: UI-логика
    |   ...                     #
    |                           #
    ├── shared/                 # Layer: Переиспользуемые ресурсы
    |   ├── api/                #         Segment: Логика запросов к API
    |   ├── lib/                #         Segment: Инфраструктурная-логика (хелперы)
    |   └── ui/                 #         Segment: UI-логика
    |   ...                     #
    |                           #
    └── index.tsx/              #
```

### Also using craco configure for good router directory - [documentation](https://craco.js.org/docs/getting-started/)