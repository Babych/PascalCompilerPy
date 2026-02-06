# Pascal Compiler

![CI Status](https://github.com/YOUR_USERNAME/pascal-compiler/workflows/Pascal%20Compiler%20CI/badge.svg)
![Quick Test](https://github.com/YOUR_USERNAME/pascal-compiler/workflows/Quick%20Test/badge.svg)
![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey)

Повнофункціональний компілятор мови Pascal, написаний на Python. Підтримує всі основні конструкції Pascal та генерує проміжний код у форматі three-address code.

## 🚀 Швидкий старт

### Windows
```cmd
python pascal_compiler.py test_simple.pas
```

або двічі клацніть `run_tests_windows.bat`

### Linux / macOS
```bash
python3 pascal_compiler.py test_simple.pas
```

або запустіть:
```bash
python3 run_tests.py
```

## ✨ Можливості

- ✅ Повна підтримка синтаксису Pascal
- ✅ Типи даних: integer, real, boolean, string, char, array
- ✅ Контрольні конструкції: if/then/else, while, for, repeat/until
- ✅ Процедури та функції з параметрами
- ✅ Семантичний аналіз та перевірка типів
- ✅ Генерація проміжного коду
- ✅ Детальні повідомлення про помилки
- ✅ Кросплатформеність (Windows, Linux, macOS)

## 📋 Вимоги

- Python 3.8 або новіший
- Без додаткових залежностей!

## 🔧 Встановлення

1. Склонуйте репозиторій:
```bash
git clone https://github.com/babych/PascalCompilerPy.git
cd pascal-compiler
```

2. Готово! Компілятор не потребує встановлення.

## 📖 Використання

### Базова компіляція
```bash
python pascal_compiler.py program.pas
```

### З детальним виводом
```bash
python pascal_compiler.py program.pas -v
```

### Збереження у файл
```bash
python pascal_compiler.py program.pas -o output.txt
```

### Допомога
```bash
python pascal_compiler.py -h
```

## 📝 Приклади

### Простий приклад
```pascal
program Hello;
var
    x: integer;
begin
    x := 42;
    writeln('The answer is: ', x)
end.
```

### Функції та процедури
```pascal
program MathExample;

function Factorial(n: integer): integer;
var
    i, result: integer;
begin
    result := 1;
    for i := 1 to n do
        result := result * i;
    Factorial := result
end;

begin
    writeln('5! = ', Factorial(5))
end.
```

Більше прикладів у файлах `test_*.pas`

## 🧪 Тестування

### Запуск всіх тестів
```bash
python run_tests.py
```

### Окремі тести
```bash
python pascal_compiler.py test_simple.pas      # Базові операції
python pascal_compiler.py test_control.pas     # Умови та цикли
python pascal_compiler.py test_functions.pas   # Функції та процедури
python pascal_compiler.py test_errors.pas      # Обробка помилок
```

## 🏗️ Архітектура

Компілятор складається з чотирьох основних фаз:

1. **Лексичний аналіз** (`lexer.py`) - Токенізація вихідного коду
2. **Синтаксичний аналіз** (`parser.py`) - Побудова AST
3. **Семантичний аналіз** (`semantic_analyzer.py`) - Перевірка типів та змінних
4. **Генерація коду** (`code_generator.py`) - Створення проміжного коду

## 📂 Структура проекту

```
pascal-compiler/
├── .github/
│   └── workflows/          # GitHub Actions CI/CD
├── pascal_compiler.py      # Головний файл компілятора
├── lexer.py               # Лексичний аналізатор
├── parser.py              # Синтаксичний аналізатор
├── ast_nodes.py           # Визначення вузлів AST
├── semantic_analyzer.py   # Семантичний аналізатор
├── code_generator.py      # Генератор коду
├── run_tests.py           # Тестовий скрипт
├── test_*.pas             # Тестові програми
└── README.md              # Документація
```

## 🤝 Внесок

Вітаються pull requests! Для великих змін спочатку відкрийте issue для обговорення.

### Як внести зміни:
1. Fork репозиторій
2. Створіть гілку (`git checkout -b feature/amazing-feature`)
3. Зробіть commit (`git commit -m 'Add amazing feature'`)
4. Push до гілки (`git push origin feature/amazing-feature`)
5. Відкрийте Pull Request

## 📊 CI/CD

Проект використовує GitHub Actions для автоматичного тестування на:
- 🐧 Linux (Ubuntu)
- 🪟 Windows
- 🍎 macOS

З версіями Python: 3.8, 3.9, 3.10, 3.11, 3.12

## 📄 Ліцензія

Цей проект надається "як є" для освітніх цілей.

## 🙏 Подяки

Створено як демонстрація технік розробки компіляторів на основі класичних принципів.

## 📞 Зворотній зв'язок

Якщо знайшли баг або маєте пропозицію - створіть [Issue](https://github.com/Babych/PascalCompilerPy/issues)!

---

**Зроблено з ❤️ для спільноти Pascal**
