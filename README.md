
# 🛡️ UNIsupport

**UNIsupport** is a modern, high-performance web-based ticket support platform specifically designed for institutional environments. It provides a seamless interface for Students, Teachers, Agents, and Administrators to manage, resolve, and audit technical and academic requests.

---

## ✨ Key Features

- **🛡️ Multi-Role Architecture**: Tailored interfaces and permissions for Students, Teachers, Support Agents, and Administrators.
- **🌐 Dual-Language Support**: Fully localized in **English** and **French** with dynamic locale switching.
- **📊 Admin Dashboard**: Real-time statistics, ticket trend charts (Chart.js), and status distribution overviews.
- **🏷️ Smart Categorization**: Intuitive ticket categories with dedicated icons and role-based visibility.
- **🔍 Advanced Audit System**: Full traceability of system actions (Creation, Update, Deletion, Login) with a searchable audit log.
- **🎨 Premium UI/UX**: Clean, professional design with a Navy Blue institutional theme, perfectly centered tables, and smooth micro-animations.
- **⚡ Real-time Updates**: Instant status changes and flash notifications for a responsive user experience.

---

## 🛠️ Tech Stack & Architecture

- **Backend**: PHP 8.1+ & [Symfony 6.4](https://symfony.com/) (LTS)
- **Database**: **SQLite** (Default) — Zero-configuration, file-based database stored in `var/data.db`.
- **Server**: **PHP Built-in Server** — Used for development to provide a lightweight, zero-dependency environment without needing Nginx/Apache.
- **Frontend**: Twig, Vanilla CSS (Premium Custom Design), JavaScript
- **Security**: RBAC (Role-Based Access Control)
- **Localization**: English & French (YAML-based)

---

## 🔐 Default Credentials

Use the following accounts to test the different role-based interfaces. Run `php bin/console app:create-users` to initialize them.

| Role | Email | Password | Permissions |
| :--- | :--- | :--- | :--- |
| **Admin** | `admin@uni.ma` | `admin123` | Full system control, Audit Logs, User Mgmt |
| **Agent** | `agent@uni.ma` | `agent123` | Manage assigned tickets, status updates |
| **Teacher** | `teacher@uni.ma` | `teacher123` | Submit requests & manage assigned tasks |
| **Student** | `student@uni.ma` | `student123` | Basic ticket submission and tracking |

---

## 🚀 Getting Started

### Prerequisites

- **PHP 8.1+** with `sqlite3` and `intl` extensions.
- **Composer** (PHP Dependency Manager).
- **Git** (for version control).

### Quick Installation

1. **Install dependencies**
   ```bash
   composer install
   ```

2. **Setup Database & User Accounts**
   ```bash
   # Create the SQLite database and run migrations
   php bin/console doctrine:database:create
   php bin/console doctrine:migrations:migrate --no-interaction

   # Seed the default users listed above
   php bin/console app:create-users
   ```

3. **Launch Development Server**
   ```bash
   # Start the lightweight PHP server
   php -S localhost:8000 -t public
   ```
   *Access the app at [http://localhost:8000](http://localhost:8000)*

---

## 💡 Why the PHP Dev Server?

We use the built-in PHP development server (`-S`) because it is **portable** and requires **zero configuration**. It allows developers to get the project running instantly without setting up complex web servers like Apache or Nginx, making it perfect for rapid prototyping and local testing.

---

## 📸 Preview

> [!TIP]
> Log in as `admin@uni.ma` to access the full Dashboard and Audit Logs management.
> (10 - 40 seconds to load)
Developed by **OMRed**
