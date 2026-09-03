# Grammar Trail — PWA / GitHub Pages

Готовый статический PWA-пакет для публикации через GitHub Pages.

## Структура

- `index.html` — интерактивный Grammar Trail.
- `manifest.webmanifest` — описание приложения для установки.
- `service-worker.js` — кэширование для офлайн-работы.
- `icon-192.png`, `icon-512.png` — иконки.
- `.nojekyll` — публикация файлов без обработки Jekyll.
- `.github/workflows/deploy.yml` — автоматический деплой GitHub Pages.

## Публикация

1. Создайте новый GitHub repository, например `grammar-trail`.
2. Загрузите **все содержимое этой папки** в корень репозитория.
3. Убедитесь, что основная ветка называется `main`.
4. В GitHub откройте `Settings → Pages`.
5. В разделе Build and deployment выберите `GitHub Actions`.
6. Сделайте push/commit — workflow автоматически опубликует приложение.
7. GitHub покажет опубликованный URL в разделе Pages / workflow deployment.

URL проекта обычно будет иметь вид:

https://ВАШ-USERNAME.github.io/grammar-trail/

## Установка на телефон

Откройте опубликованный HTTPS-адрес:
- iPhone: Safari → «Поделиться» → «На экран Домой».
- Android: Chrome → меню → «Установить приложение» / «Добавить на главный экран».

После первого запуска service worker кэширует приложение, поэтому основной интерфейс сможет работать без сети.

## Важно

Не открывайте `index.html` через Files как обычный локальный файл. Для PWA нужен HTTP(S)-адрес.

Все данные дашборда остаются внутри `index.html`; внешние библиотеки для его работы не требуются.
