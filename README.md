# Flask Projects Manager

#### Description:

**Flask Projects Manager** is a Python **web application** built with Flask that allows users to register, log in, create projects, and add tasks under each project. The application demonstrates user authentication, form validation, database relationships, and template rendering in Flask. It provides a clean and minimal interface for task and project tracking.


---

## Project Purpose
The main goal of this project is to practice and showcase fundamental **Flask web development concepts** such as authentication, database management with SQLAlchemy, password hashing, session handling, and form validation.

This app helps users manage their personal projects and related tasks in a simple, lightweight environment. Each user can:

- Create their own account.
- Log in.
- Add one or more projects.
- Add multiple tasks for each project.

---

## File Descriptions

- **app.py**: The main Flask application. Contains routes, models, and configuration.
- **templates/**: Contains HTML templates rendered with Jinja2.
  - `main.html` → Welcome page with links to login/register.
  - `login.html` → User login form.
  - `register.html` → User registration form with password confirmation.
  - `project.html` → Project list and project creation page.
  - `task.html` → Task management page for each project.
- **requirements.txt**: Lists Python dependencies for the project.



---

## Technologies and Libraries Used

- **Python 3**
- **Flask** – micro web framework
- **Flask-SQLAlchemy** – ORM for SQLite
- **Flask-Login** – session and authentication handling
- **Flask-WTF** + **WTForms** – forms and CSRF protection
- **Flask-Bcrypt** – password hashing

---

## Design Decisions

- **Authentication & Security**:
  Implemented with Flask-Login. Passwords are never stored in plain text but hashed with Bcrypt. Sessions are secured with a `SECRET_KEY`.

- **Database Schema**:
  A simple relational model was chosen:
  - One user → many projects.
  - One project → many tasks.
  This clear structure makes it easy to expand the app later.

- **Templates & Styling**:
  Minimal HTML/CSS (no external frameworks) was chosen to focus on backend logic. Inline styles keep the app lightweight but can be refactored into a `templates/` folder.

- **Form Validation**:
  Flask-WTF was used to ensure input validation (e.g., password confirmation, unique usernames).

---

## Usage

When the app runs, users interact through the browser:

1. Install requirements:
   ```bash
   pip install -r requirements.txt
   ```

2. Run the application:
   ```bash
   python app.py
   ```

3. The terminal will display something like:
   ```
   * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
   ```
   ➜ Click the link in the terminal to open the app in your browser.

---
## Acknowledgements

## Acknowledgements

This project was partially inspired by community examples on Flask authentication with SQLAlchemy.
The login and register structures were adapted from existing Flask + SQLAlchemy tutorials, and then customized and extended for this project’s needs:

- Tutorial Repository: [Python Flask Authentication Tutorial](https://github.com/neupanic/Python-Flask-Authentication-Tutorial.git)


---

## Conclusion

**Flask Projects Manager** is a lightweight demonstration of authentication, form validation, and database handling in Flask. It provides a simple way to register, log in, and manage projects with tasks.

ℹ️ **Important Notes for Users:**
- If the password and confirm password fields do not match during registration, the registration form will simply refresh. The user needs to re-enter the password, but no explicit warning message is displayed yet.
- If a user tries to log in with a username that is not registered, the page also refreshes without showing a warning.

These behaviors are intentional in this basic version, but they can be improved by adding **flashing messages** or **form error displays** in the future.  
---

---
*Prepared by:* [Başak Yaralı]
*Github:* [byart0]
*Date Saved:* 2025-09-07
*Location:* [İstanbul, Türkiye]
*e-mail:* [basakyarali@gmail.com]
---

---

