# Каталог учебной библиотеки

Практическая работа №2 по дисциплине «Технологии разработки программного обеспечения».

## Описание

Адаптивный каталог учебных материалов с фильтрацией по категориям.
Интерфейс построен на HTML5, SCSS и CSS Grid.  
Данные берутся из `data/catalog.csv`, цвета и размеры — из `data/theme.json`.

## Технологии

- HTML5
- SCSS / Sass
- CSS Grid и Flexbox
- Git

## Структура проекта


tpro-pr02-student/
├── css/
│   └── styles.css                 # Скомпилированный CSS
├── scss/
│   ├── styles.scss                # Главный файл SCSS
│   ├── _variables.scss            # SCSS-переменные
│   ├── _mixins.scss               # SCSS-mixins
│   ├── _base.scss                 # Базовые стили
│   ├── _layout.scss               # Раскладка страницы
│   └── components/
│       ├── _card.scss             # Карточка товара
│       ├── _filter.scss           # Панель фильтров
│       └── _badge.scss            # Бейдж категории
├── data/
│   ├── catalog.csv                # Исходные данные каталога
│   └── theme.json                 # Цвета, радиус и отступы
├── images/
│   ├── product-01.svg
│   ├── product-02.svg
│   └── product-03.svg
├── index.html                     # Главная страница
├── package.json
├── .gitignore
└── README.md


## Требования к окружению

- Node.js LTS
- npm

## Установка и запуск

1. Клонируйте репозиторий:

```bash
git clone https://github.com/i-GeKa-i/tpro-pr02-student.git
cd tpro-pr02-student
```

2. Установите зависимости:

```bash
npm install
```

3. Скомпилируйте SCSS в CSS:

```bash
npm run build
```

4. Откройте `index.html` в браузере.

### Режим разработки

Для автоматической перекомпиляции при изменении SCSS:

```bash
npm run watch
```

## Проверка

Откройте страницу в Chrome DevTools и проверьте отображение на ширинах:

- 1440 px — десктоп, фильтры слева
- 768 px — планшет, фильтры переносятся над каталогом
- 375 px — мобильный, одна колонка

Горизонтальной прокрутки быть не должно.

## Особенности

- Используются SCSS-переменные для цветов, отступов и радиуса.
- Повторяющееся оформление категорий вынесено в mixin.
- Адаптивная сетка карточек — через `grid` с `auto-fit` и `minmax`.
- Два breakpoints: 768 px и 375 px.

## Источники

- Данные предоставлены в рамках учебного задания.
- HTMLBook — https://htmlbook.ru
- Документация Sass — https://sass-lang.com/documentation