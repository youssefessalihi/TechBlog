# 📚 TechBlog - Plateforme de Blog   
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
- [.NET SDK 9.0]
- [SQL Server]
- [Git]
---
### 1. Cloner le dépôt
```bash
git clone https://github.com/youssefessalihi/TechBlog

cd TechBlog
```
### 2. Configurer la base de données

- Ouvrir `appsettings.json` et configurer la chaîne de connexion à votre base de données SQL Server.
```json
{
  "ConnectionStrings": {
	"DefaultConnection": "Server=localhost;Database=TechBlogDB;User Id=sa;Password=your_password;"
  },
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
---

### 5. Screenshot
#### Home:
![image](https://github.com/user-attachments/assets/ee700107-5298-474a-b359-6d75c876d903)
![image](https://github.com/user-attachments/assets/f51fda9f-af4c-4f22-b075-80b07826653b)
![image](https://github.com/user-attachments/assets/d1e73a10-b7df-4be1-bd5e-e1fe1145527a)
![image](https://github.com/user-attachments/assets/80156e37-c262-4930-a457-20335fc8ac34)
#### Admin:
![image](https://github.com/user-attachments/assets/ca09c75b-b260-425f-87be-af69d0f39ab9)
![image](https://github.com/user-attachments/assets/b0813778-0650-4229-8da0-51fd996ae331)

#### Auteur:
![image](https://github.com/user-attachments/assets/f148d2be-53b6-4a15-aea5-78f4e1eaf047)


### Développé avec passion 💻 dans le cadre académique de SupMTI.

