criptooTRXbot - Mini App Telegram

1) Publica index.html en un sitio HTTPS, por ejemplo GitHub Pages.
2) En Monetag, crea/configura una Telegram Mini App y copia el script SDK completo que genera el panel.
3) Pega ese script en el <head> de index.html, sustituyendo el comentario de ejemplo. No inventes la URL del SDK.
4) Edita MINIAPP_URL en el .ino con la URL HTTPS final de GitHub Pages.
5) Sube el .ino al ESP32 y abre /start en el bot.
6) Los botones Mini App transmiten acciones con Telegram WebApp sendData; el ESP32 las procesa al recibir web_app_data.

Limitaciones:
- La Mini App necesita HTTPS público, no basta con servirla desde el ESP32 por HTTP local.
- La recompensa publicitaria enviada desde el cliente no es antifraude. Para recompensas robustas, Monetag recomienda postback server-side; un ESP32 autónomo sin endpoint público no puede recibir esos postbacks de forma fiable.
- No publiques el .ino con credenciales. Las claves que estaban en el código anterior se han considerado expuestas y deberían rotarse.
