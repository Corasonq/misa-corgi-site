# Corgi Misa Cyber Cozy Site

Одностраничный сайт про корги Мису. Работает без сборки: достаточно открыть или загрузить `index.html`.

## Как поменять фото и видео

Открой `index.html` и замени ссылки:

- Фото: теги `<img ... src="...">`
- Видео: теги `<video ... src="...">`

Подходят прямые ссылки на изображения `.jpg`, `.png`, `.webp` и видео `.mp4`, `.webm`.

## Как загрузить на GitHub

```bash
git init
git add .
git commit -m "Add Misa website"
git branch -M main
git remote add origin https://github.com/USERNAME/REPOSITORY.git
git push -u origin main
```

## Как скачать на VPS

```bash
cd /var/www
sudo git clone https://github.com/USERNAME/REPOSITORY.git misa
```

## Пример Nginx

```nginx
server {
    listen 80;
    server_name your-domain.com;
    root /var/www/misa;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }
}
```

Потом:

```bash
sudo nginx -t
sudo systemctl reload nginx
```
