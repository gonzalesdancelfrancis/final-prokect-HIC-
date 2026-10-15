# Spotibai

A small Django web app with clickable pages, based on a Figma wireframe. The login and account creation pages are visual prototypes; they do not save or authenticate accounts.

## Run it

```bash
pip install -r requirements.txt
python manage.py runserver
```

Open http://127.0.0.1:8000/login/. **Create one** opens the signup form; submitting it returns to login. The demo **Log in** button opens Home.

## Pages

- `/register/` signup form prototype
- `/login/` login form prototype
- `/` home
- `/play/<id>/` song page with previous and next icons
- `/account/` account
- `/liked/`, `/recent/`, `/trending/` song lists
- `/playlists/` and `/playlists/<id>/` playlists

## Where things are

- `music/data.py` the songs, playlists and which songs each list shows
- `music/views.py` one short view per page
- `music/templates/base.html` the shared page: head, sidebar, header, footer. Pages extend it and fill in their own content
- `music/templates/tunes/song_card.html` the song card that pages include
- `music/static/style.css` all styling; the color palette is the variables at the top
