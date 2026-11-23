# Инструкция по публикации на GitHub Pages / Vercel

Сайт полностью готов и уже собран в git-репозиторий. Осталось только
создать репозиторий на GitHub и запушить.

## Что в архиве `site-publish.zip`

- `index.html` — весь сайт (один файл: Tailwind CSS + Google Fonts + FontAwesome с CDN)
- `README.md` — описание проекта
- `LICENSE` — MIT
- `CONTRIBUTING.md` — правила участия
- `.git` — уже инициализированный репозиторий (ветка `main`, коммит «Initial commit»)

## Вариант 1. GitHub Pages (рекомендуется для открытого сайта)

1. Создайте **пустой** репозиторий на github.com (без README, без .gitignore).
2. Распакуйте архив в папку и выполните:

```bash
git remote add origin https://github.com/<ваш-логин>/<имя-репозитория>.git
git branch -M main
git push -u origin main
```

3. Включите GitHub Pages: **Settings → Pages → Source: Deploy from a branch → main / (root) → Save**.
4. Сайт появится по адресу: `https://<ваш-логин>.github.io/<имя-репозитория>/`

## Вариант 2. Vercel (если удобнее)

1. Загрузите репозиторий на GitHub (шаги 1–2 выше).
2. На vercel.com выберите **Add New → Project** и импортируйте этот репозиторий.
3. Настройки по умолчанию подойдут (статический сайт, фреймворк не нужен).
4. Vercel выдаст адрес вида `https://<проект>.vercel.app`.

## Примечания

- Сайту нужен интернет только для CDN (Tailwind, шрифты, FontAwesome).
- Имя автора в коммите сейчас placeholder — при необходимости поправьте:
  `git config user.name "Ваше Имя" && git config user.email "you@example.com"` перед коммитом.
- Если репозиторий планируется публичным — откройте его (по умолчанию GitHub создаёт приватные; для Pages это тоже работает).
