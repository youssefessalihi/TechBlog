# 📚 TechBlog - Plateforme de Blog Académique  
*Projet réalisé dans le cadre du module .NET à SupMTI*  
**Encadré par** : M. Omari  
**Équipe** : Youssef Essalihi, Zineb Harza, Aya Boubekri, Wadie Makich, Halima Elyousfi  

---

## 🎯 Objectif  
Développer une plateforme de blog complète avec :  
- **Gestion de contenu** (articles, pages statiques)  
- **Authentification sécurisée** (rôles Admin/Auteur)  
- **Dashboard administrateur**  
- **SEO optimisé** (slugs, métadonnées)  
- **Responsive design** (adapté mobile/desktop)  

---

## 🚀 Fonctionnalités  

### 🌍 Frontend (Public)  
- 📰 Affichage paginé des articles (`X.PagedList`)  
- 🔍 Pages statiques : `/about`, `/contact`, `/privacy`  
- 📱 Interface responsive avec **Bootstrap 5**  
- ✨ Animations et notifications toast (`AspNetCoreHero.ToastNotification`)  

### 🔧 Backend (Admin)  
- 🔐 **Authentification** :  
  - Création de comptes (Admin/Auteur)  
  - Réinitialisation de mot de passe  
  - Gestion des rôles via ASP.NET Identity  
- 🖼️ **Gestion de contenu** :  
  - CRUD d'articles avec upload d'images (`/wwwroot/thumbnails`)  
  - Édition des pages statiques  
  - Génération automatique de slugs (SEO)  
- ⚙️ **Configuration** :  
  - Personnalisation du titre du site  
  - Liens vers réseaux sociaux (Facebook, Twitter, GitHub)  

---

## 🛠️ Stack Technique  

### Backend  
- **Framework** : ASP.NET Core 9.0  
- **Base de données** : SQL Server + Entity Framework Core  
- **Sécurité** : ASP.NET Identity (+ Hash PBKDF2)  
- **Bibliothèques** :  
  - `X.PagedList.Mvc.Core` (pagination)  
  - `AspNetCoreHero.ToastNotification` (notifications)  

### Frontend  
- **UI/UX** : Bootstrap 5 + AdminLTE (dashboard)  
- **Outils** : jQuery, DataTables (tableaux interactifs)  
- **Stockage** : Images sauvegardées dans `/wwwroot/thumbnails`  

---

## 📂 Structure du Projet  
```bash
TechBlog/
├── Areas/
│   └── Admin/                 # Zone administrateur
│       ├── Controllers/       # 🎮 PostController, PageController, UserController
│       └── Views/             # 🖌️ Vues Razor (CRUD, paramètres)
├── Controllers/               # 🎮 HomeController, BlogController (frontend)
├── Data/                      # 🗃️ ApplicationDbContext + Migrations
├── Models/                    # 📦 Entités : Post, Page, ApplicationUser
├── ViewModels/                # 📤 DTOs : PostVM, PageVM, RegisterVM
├── wwwroot/                   # 🌐 Assets statiques
│   ├── thumbnails/            # 🖼️ Images uploadées
│   ├── Dashboard/             # 🎨 Template AdminLTE
│   └── lib/                   # 📚 Bibliothèques (Bootstrap, jQuery)
└── appsettings.json           # ⚙️ Configuration (chaîne de connexion DB)
```
## 🛠️ Installation & Configuration

### Prérequis
- [.NET SDK 9.0](https://dotnet.microsoft.com/download)
- [SQL Server](https://www.microsoft.com/fr-fr/sql-server/sql-server-downloads) (ou SQL Server Express)
- [Git](https://git-scm.com/downloads)

### 1. Cloner le dépôt
```bash
git clone https://github.com/youssefessalihi/TechBlog
cd TechBlog

### 2. Configurer la base de données

- Ouvrir `appsettings.json` et configurer la chaîne de connexion à votre base de données SQL Server.
```json
{
  "ConnectionStrings": {
	"DefaultConnection": "Server=localhost;Database=TechBlogDB;User Id=sa;Password=your_password;"
  },
  ...
}
```
### 3. Appliquer les migrations
```bash
dotnet ef database update
```
### 4. Lancer l'application
```bash
dotnet run
```

### Développé avec passion 💻 dans le cadre académique de SupMTI.

