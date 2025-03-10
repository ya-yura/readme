# Erston: Онбординг и документация

Добро пожаловать в Erston – язык программирования, созданный специально для платформы Cleverence. Данный гайд поможет вам быстро освоить синтаксис Erston, развернуть среду разработки и написать первое приложение.

## 📌 Введение
Erston разработан для удобного создания бизнес-приложений на платформе Cleverence. Он сочетает строгость типизированного языка и удобство декларативного описания интерфейсов.

## 🚀 Установка и настройка
Перед началом работы необходимо установить Erston SDK. 

### 1. Установка Erstudio (GUI)
Erstudio – официальная среда разработки для Erston. Чтобы её установить:
```sh
curl -L -o erstudio_installer.sh https://cleverence.com/download/erstudio
chmod +x erstudio_installer.sh
./erstudio_installer.sh
```

### 2. Установка CLI-компилятора
Если вы предпочитаете работать в терминале, установите CLI-версию:
```sh
curl -L -o erston-cli https://cleverence.com/download/erston-cli
chmod +x erston-cli
mv erston-cli /usr/local/bin/erston
```

## ✍️ Основы синтаксиса
### Переменные и типы
Erston поддерживает строгую типизацию:
```erston
let a: int = 42;
let b: string = "Hello, world!";
let c: bool = true;
```

### Функции
```erston
func sum(a: int, b: int) -> int {
    return a + b;
}
```

## 🔌 Работа с платформой Cleverence
### Подключение API
```erston
let response = http.get("https://api.cleverence.com/data");
if response.status == 200 {
    log(response.body);
}
```

## 📊 Работа с базой данных
Erston включает встроенную ORM:
```erston
let users = db.query<User>().where(u -> u.age > 18).toList();
```

## 🎨 Создание UI
Erston позволяет создавать декларативные интерфейсы:
```erston
ui {
    button "Нажми меня" {
        on click {
            log("Кнопка нажата!");
        }
    }
}
```

## ⚠️ Обработка ошибок
```erston
try {
    let data = api.fetch("/data");
} on fail {
    log("Ошибка загрузки данных");
}
```

## 🛠 Практический пример
Напишем простое приложение, которое загружает список товаров и отображает их в таблице:
```erston
ui {
    table {
        columns: ["Название", "Цена"]
        rows: db.query<Product>().toList();
    }
}
```

## 🎯 Заключение
Вы освоили базовые принципы Erston! Дальше можно углубляться в документацию и разрабатывать сложные приложения на Cleverence.
