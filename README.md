<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f766e,100:2dd4bf&height=170&section=header&text=Chat%20App%20PHP&fontColor=ffffff&fontSize=44&fontAlignY=38&desc=A%20browser-based%20one-to-one%20chat%20application&descAlignY=60&descSize=16" alt="Chat App PHP" />

![PHP](https://img.shields.io/badge/PHP-7-777bb4?style=flat-square&logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-database-4479a1?style=flat-square&logo=mysql&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-vanilla-f7df1e?style=flat-square&logo=javascript&logoColor=black)
![AJAX](https://img.shields.io/badge/AJAX-chat%20updates-333333?style=flat-square)

</div>

A browser-based one-to-one chat application built with PHP, MySQL, and JavaScript. Users can register, sign in, browse other users, and exchange messages through PHP endpoints.

## ✨ Features

- Signup and login forms with session-based authentication.
- User directory and user-name search.
- One-to-one message send and conversation display.
- User avatars and active-status updates in the application flow.
- `chatapp.sql` defines the `users` and `messages` tables.

## 🏗️ Architecture

PHP pages render signup, login, user-list, and conversation views. JavaScript sends AJAX requests to PHP scripts under `php/`; these scripts use `mysqli` to read or write the MySQL database. There is no separate API server or WebSocket service in this repository.

## 🧰 Tech stack

| Area | Technology |
| --- | --- |
| Server | PHP |
| Database | MySQL / MariaDB with `mysqli` |
| Browser | HTML, CSS, JavaScript, AJAX |
| Local web server | Apache or another PHP-capable server |

## 🚀 Getting started

1. Install PHP with the `mysqli` extension and MySQL or MariaDB, plus a local PHP web server (for example, XAMPP).
2. Create a database named `chatapp` and import `chatapp.sql` using phpMyAdmin or the MySQL client.
3. Review `php/config.php` and configure the database host, username, password, and database name. The committed values assume a local MySQL setup.
4. Serve the repository from the web server's document root and open `index.php` in a browser.
5. Ensure the app's image-upload directory is present and writable by PHP when testing signup with an avatar.

## 📁 Project structure

```text
├── index.php / login.php / users.php  # Signup, login, user list
├── chat.php                            # Conversation page
├── php/config.php                      # Database connection
├── php/                                # AJAX and database handlers
├── javascript/                         # Browser interactions
└── chatapp.sql                         # Database schema
```

## 🗺️ Roadmap / Notes

- This is a small learning project; it has no dependency manifest, automated tests, or production deployment configuration.
- The database settings are hard-coded for a local environment and must be changed before deployment.
- The login implementation compares MD5 password hashes; MD5 is not suitable for password storage in a production application.

## 👤 Author

**Brian Dol**, Senior Full Stack Engineer · [Portfolio](https://portfolio.briandol.workers.dev/) · [LinkedIn](https://linkedin.com/in/brian-dol-31a06115a/)
