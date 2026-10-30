# Стайлгайд документации системы распознавания рукописного текста

Лабораторная работа 3 по разработке и оформлению проектной документации.
Проект содержит правила, два документа для апробации, оценку качества,
линтинг Markdown и автоматическую сборку и публикацию MkDocs.

## Начало работы

```powershell
python -m venv .venv
.venv\Scripts\python -m pip install -r requirements.txt
npm ci
npm run lint
.venv\Scripts\python -m mkdocs build --strict
.venv\Scripts\python -m mkdocs serve
```

В Linux и macOS используйте `.venv/bin/python` вместо `.venv\Scripts\python`.
Нужны Python 3.12 и Node.js 22 или новее. Сервер покажет адрес локального сайта.

## Состав работы

- [Правила](docs/index.md).
- [Инструкция пользователя](docs/examples/user-guide.md).
- [Протокол проверки](docs/examples/test-protocol.md).
- [Оценка качества](docs/evaluation.md).
- [Отчёт по заданию](REPORT.md).
- [Порядок внесения изменений](CONTRIBUTING.md).

## Публикация

В настройках репозитория откройте **Settings → Pages → Build and deployment**
и выберите **Source → GitHub Actions**. После успешных проверок коммит в `main`
публикуется по адресу <https://qwertyums.github.io/style-guide-project/>.
PR только проверяется; его содержимое не публикуется до слияния.

## Границы примеров

Документация относится к учебной модели продукта. Названия кнопок и сценарии
в примерах задают согласованный макет поведения. Они не подтверждают наличие
реализованного приложения, поддерживаемых форматов или измеренной точности.
