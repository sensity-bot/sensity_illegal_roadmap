
# 🤖 ANØM – Bot Discord pour Sensity*

**ANØM** est un bot Discord conçu pour le serveur Sensity illégal.  
Il permet la création d’un marché clandestin, avec annonces, rappels, notifications personnalisées et gestion automatisée pour les GM.

---

## 🚀 Fonctionnalités principales

### 🛒 Marketplace (`/market`)

- Créer une annonce via une interface :
  - Catégorie : `Armes`, `Stupéfiants`, `Utilitaires`
  - Sous-produit, quantité, numéro, prix
- Affichage des annonces dans un embed
- Suppression d’une annonce par son auteur uniquement avec `/market remove`
- Voir les 5 **meilleurs prix** pour un sous-produit avec `/market best`

### 🔔 Notifications (`/notif`)

- `/notif subscribe` : s’abonner à un sous-produit
- À chaque nouvelle annonce, une notification dans le canal avec **mention**
- `/notif list` : voir ses abonnements actifs
- `/notif unsubscribe` : se désabonner avec id


### 📣 Messages de masse (`/message`) pour GM (en dev)

> **Admins uniquement**

- Envoi d’un MP à tous les membres d’un rôle spécifique

### ⚙️ Automatisations

- 🔁 Rappel automatique à l’auteur d’une annonce après **5 jours**
- 🧹 Suppression automatique des annonces après **15 jours**

---

## 🧑‍🏫 Guide pour les joueurs

### ➕ Créer une annonce
```bash
/market add
````

Suivez l’UI (catégorie, sous-produit, etc.), l’annonce est postée automatiquement.

### ❌ Supprimer son annonce

```bash
/market remove ID
```

### 🔎 Voir les meilleures offres

```bash
/market best
```

### 📬 Gérer les notifications

```bash
/notif subscribe
/notif list
/notif unsubscribe
```



---

## ❓ FAQ

### Que se passe-t-il après 15 jours ?

L’annonce est automatiquement supprimée.

### Les notifs sont-elles en MP ?

Non, elles sont envoyées **dans le canal** où l’abonnement a été fait, avec mention.

### Peut-on étendre la durée d’une annonce ?

Non, il faut la republier.
