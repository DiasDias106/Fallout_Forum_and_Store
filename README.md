<h1 align="center">☢️ Fallout Forum & Webstore</h1>

<p align="center">
  <i>A Fallout-themed community website with a forum, minigames with leaderboards, a full webstore, and an admin back office. Built with PHP and MySQL.</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP"/>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript"/>
  <img src="https://img.shields.io/badge/Bootstrap-5.3-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white" alt="Bootstrap"/>
  <img src="https://img.shields.io/badge/PHPMailer-email-1a1b27?style=for-the-badge" alt="PHPMailer"/>
</p>

---

## 📖 About

**Fallout Forum & Webstore** is a full-stack web platform set in the *Fallout* universe. Visitors can read about the lore, play minigames and compete on leaderboards, subscribe to a newsletter, and buy themed merchandise. Administrators manage users and the store catalogue through a dedicated back office.

## ✨ Features

### 🌐 Community & Content
- 📚 **Lore pages** about the Fallout universe, backed by a custom JSON dataset (`Fallout_API.json`)
- 🎵 **Music library** with tracks from across the franchise
- 🌳 **TreeView** for browsing resources and downloads
- 🔍 **Live search** (AJAX)

### 🎲 Minigames & Tools
- 🪢 **Hangman**, 🔢 **Number guessing**, 🎲 **Dice game**: scores saved to the database
- 🏆 **Leaderboards** comparing players' scores
- 🧮 Calculator, 💱 currency converter, 📅 day counter, 🔒 "Seal Algorithm"

### 🛒 Webstore
- Browse **games, figures and other merchandise**
- 🛍️ **Shopping cart** and **purchase history**

### 🔐 Accounts & Admin
- **Sign up, login and profile editing**
- 🧑‍💼 **Admin area**: add, edit and remove store items (games, figures, others) and manage users

### ✉️ Email
- **Newsletter** subscription and a **contact form**, sent via **PHPMailer** over Gmail SMTP

## 🚀 Getting Started

### Requirements
- **PHP 8+** and **MySQL / MariaDB**, for example through [XAMPP](https://www.apachefriends.org/)
- [Composer](https://getcomposer.org/) (for PHPMailer)

### Setup
1. Clone the repository into your web server folder (e.g. `xampp/htdocs`):
   ```bash
   git clone https://github.com/DiasDias106/Fallout_Forum_and_Store.git
   ```
2. Install PHPMailer inside `Fallout_forum_and_store/Fallout_forum_and_store/`:
   ```bash
   composer require phpmailer/phpmailer
   ```
3. Create a MySQL database named **`forum`** with the tables used by the app: `utilizadores`, `jogos`, `figuras`, `outros`, `venda`, `paginas`, `forca`, `adivinhanumero`, `jogodados`.
4. Set your database credentials in `cnn.php` and `cnn1.php`:
   ```php
   $user = 'Seu_User';
   $pass = 'Sua_Senha';
   ```
5. *(Optional)* For email features, add your Gmail address and an **App Password** in `mail2.php` and `newsletter.php`.
6. Start Apache and MySQL, then open `http://localhost/Fallout_Forum_and_Store/Fallout_forum_and_store/Fallout_forum_and_store/`.

> 🔒 Never commit real credentials. Keep them local or move them to environment variables.

## 📁 Project Structure

```
Fallout_forum_and_store/Fallout_forum_and_store/
├── *.php / *.html          # Pages: forum, store, cart, login, admin, minigames…
├── cnn.php, cnn1.php       # PDO database connection
├── mail2.php, newsletter.php
├── Fallout_API.json        # Lore dataset (factions, locations, characters…)
├── bootstrap-5.3.3-dist/js # Bootstrap + custom scripts (cart, games, search, treeview…)
├── css/                    # Stylesheets
├── imagens/, imagens_loja/ # Site and store images
├── figuras/, jogos/, outros/  # Store product images
└── musicas/                # Soundtrack files
```

## 🛠️ Built With

| Layer | Technology |
|-------|------------|
| Front end | HTML5, CSS3, JavaScript, Bootstrap 5.3 |
| Back end | PHP (PDO, sessions) |
| Database | MySQL |
| Email | PHPMailer (SMTP) |
| Data | JSON |

## ⚠️ Disclaimer

Fan-made educational project. *Fallout* and all related names and assets belong to Bethesda Softworks.

---

<p align="center">Made by <a href="https://github.com/DiasDias106">Francisco Dias</a></p>
