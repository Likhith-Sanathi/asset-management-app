
## flask-asset-management

A lightweight asset-management web application built with Flask. This repository contains the Flask app, templates, static assets, and SQL schema used for a college project.

**Features**
- User authentication (login / sign up)
- Add, edit, update, sell and log assets
- Dashboard and insights pages
- SQL schema included for easy local setup

**Prerequisites**
- Python 3.8+
- Git (optional)

**Quick Installation (Windows)**

1. Clone the repo (or download the source):

```powershell
git clone https://github.com/<your-username>/flask-asset-management.git
cd "flask-asset-management"
```

2. Create and activate a virtual environment:

```powershell
python -m venv venv
.\\venv\Scripts\Activate.ps1    # PowerShell
# or for cmd.exe use:
.\\venv\Scripts\activate.bat
```

3. Install dependencies:

```powershell
pip install Flask Flask-Session
# Or if a requirements file exists:
pip install -r requirements.txt
```

4. Prepare the database

This project includes `schema.sql` and `query.sql` at the repository root. Example using SQLite:

```powershell
sqlite3 caflask.db < schema.sql
sqlite3 caflask.db < query.sql    # optional seed queries
```

If you use Postgres/MySQL, run the SQL files with the appropriate client and update connection settings in `database.py`.

5. Set environment variables

Create a `.env` file or set env vars in your shell. Typical variables:

```powershell
$env:FLASK_APP = "app.py"
$env:FLASK_ENV = "development"
$env:SECRET_KEY = "your-secret-key"
```

6. Run the app

```powershell
flask run
# or
python app.py
```

Open http://127.0.0.1:5000/ in your browser.

**Quick Installation (macOS / Linux)**

```bash
git clone https://github.com/<your-username>/flask-asset-management.git
cd flask-asset-management
python3 -m venv venv
source venv/bin/activate
pip install Flask Flask-Session
sqlite3 caflask.db < schema.sql
sqlite3 caflask.db < query.sql
export FLASK_APP=app.py
export FLASK_ENV=development
export SECRET_KEY="your-secret-key"
flask run
```

**Project Structure**

- `app.py` — main Flask application entry
- `database.py` — database helpers / connections
- `forms.py` — form helpers
- `schema.sql` / `query.sql` — SQL schema and optional seed queries
- `templates/` — Jinja2 HTML templates
- `static/` — CSS, fonts, and other static assets

**Notes**
- Update DB connection settings in `database.py` if you use a non-SQLite DB.
- For production, run behind a WSGI server (Gunicorn, uWSGI) and store secrets securely.

**Contributing**

Contributions welcome — open issues or pull requests for fixes and improvements.

**License**

Add a `LICENSE` file to declare project licensing.

![image_alt](https://github.com/PixelManiac-Droid/asset-management-app/blob/757bd8cf69b6286fd52935bd5b2cb7efcfb38ee5/Screenshot%202025-04-09%20145721.png)

![image_alt](https://github.com/PixelManiac-Droid/asset-management-app/blob/757bd8cf69b6286fd52935bd5b2cb7efcfb38ee5/Screenshot%202025-04-09%20145743.png)

![image_alt](https://github.com/PixelManiac-Droid/asset-management-app/blob/757bd8cf69b6286fd52935bd5b2cb7efcfb38ee5/Screenshot%202025-04-09%20145817.png)

![image_alt](https://github.com/PixelManiac-Droid/asset-management-app/blob/757bd8cf69b6286fd52935bd5b2cb7efcfb38ee5/Screenshot%202025-04-09%20145829.png)

![image_alt](https://github.com/PixelManiac-Droid/asset-management-app/blob/757bd8cf69b6286fd52935bd5b2cb7efcfb38ee5/Screenshot%202025-04-09%20145829.png)

![image_alt](https://github.com/PixelManiac-Droid/asset-management-app/blob/757bd8cf69b6286fd52935bd5b2cb7efcfb38ee5/Screenshot%202025-04-09%20145843.png)

![image_alt](https://github.com/PixelManiac-Droid/asset-management-app/blob/9131f7792e5afa8c5d842283478b1df346e77eeb/Screenshot%202025-04-09%20145855.png)

