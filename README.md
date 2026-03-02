# 🏢 Bagisto Users & Roles Module

Transform your Bagisto store into a powerful B2B platform with advanced company user and role management.

---

## 📖 Introduction

The **Bagisto Users & Roles Module** enhances a standard Bagisto storefront by enabling business customers to manage internal company users (employees/staff) and assign them granular roles and permissions.

Built with a completely decoupled architecture, this module ensures:

- ✅ Zero modifications to Bagisto core files  
- ✅ Safe future Bagisto upgrades  
- ✅ Seamless integration with Bagisto 2.x UI (Tailwind CSS)

---

## ✨ Key Features

### 👥 Company Users Management

Allow customers to:

- Create multiple sub-users under a single company account  
- Edit, update, and manage employee access  
- Assign roles dynamically  

---

### 🔐 Roles & Permissions System

- Create fully custom roles  
- Use a dynamic nested permission tree  
- Enable “All Access” or selective granular permissions  

---

### 🎨 Seamless UI Integration

- Injects native-looking menu items inside the Customer Profile sidebar  
- Fully responsive  
- Built using Bagisto Blade components  

---

### 🧩 Isolated & Scalable Architecture

- Uses **Konekt Concord**  
- Contract & Proxy-based structure  
- No core file overrides  
- Fully modular and upgrade-safe  

---

## ⚙️ Requirements

Ensure your environment meets the following:

| Requirement | Version |
|------------|----------|
| **Bagisto** | v2.3.x or higher |
| **PHP** | ^8.2 |
| **Composer** | v2.0+ |

---

## 📌 Compatibility

- Compatible with Bagisto 2.x  
- Designed for Laravel 11 environments  
- Follows PSR-4 autoloading standards  

---

## 🚀 Installation Guide

### Step 1: Add Repository

Open your Bagisto root `composer.json` and add:

```json
"repositories": [
    {
        "type": "vcs",
        "url": "https://github.com/YOUR-USERNAME/bagisto-b2b-account"
    }
]
```
*(Replace `YOUR-USERNAME` with your actual GitHub username).*

### Step 2: Require the Package
Run the following command in your terminal to pull the module into your Bagisto store:

```bash
composer require acme/b2b-account:dev-main
```

### Step 3: Register the Service Provider
Tell Bagisto to load your new module. Open `bootstrap/providers.php` and add the Service Provider to the end of the returned array:

```php
return [
    // ... other providers
    Acme\B2BAccount\Providers\B2BAccountServiceProvider::class,
];
```
## Step 4: Run the Installation Command
Finally, run the custom Artisan command included with this package. This will automatically execute the database migrations and clear your application cache:

```bash
php artisan b2b-account:install
```

🎉 **That's it!** Log in to your Bagisto storefront as a customer, navigate to your profile, and you will see the new "Company Users" and "Roles & Permissions" tabs in your sidebar.

---

## 🛠️ Usage
1. **Create a Role:** Navigate to `Roles & Permissions` -> `Add Role`. Choose either "All Access" or select specific capabilities from the custom permissions tree.
2. **Create a User:** Navigate to `Company Users` -> `Add User`. Fill in the employee's details, assign them the role you just created, and save. The system will auto-generate a secure password for them.
