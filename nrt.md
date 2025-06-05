# ✅ Procédure de test NRT – Bot Discord ANØM (Sensity)

## 🔁 À exécuter à chaque évolution de code pour éviter les régressions.

---

## 🛒 Marketplace (/market)

### ➕ Création d'annonce
- [ ] Exécuter `/market add`
- [ ] Vérifier affichage de l’UI (catégorie, sous-produit, quantité, numéro, prix)
- [ ] Soumettre l’annonce
- [ ] Confirmer l’apparition correcte dans un embed, dans le bon canal

### ❌ Suppression d’annonce
- [ ] Exécuter `/market remove ID` avec un ID valide appartenant à l’utilisateur → succès
- [ ] Essayer de supprimer une annonce qui n’appartient pas à l’auteur → échec (message d’erreur)

### 🔎 Meilleures offres
- [ ] Exécuter `/market best` pour un sous-produit avec plusieurs annonces
- [ ] Vérifier tri des 5 annonces les moins chères
- [ ] S’assurer qu’aucune annonce expirée ne s’affiche

---

## 🔔 Notifications (/notif)

### 📥 Abonnement
- [ ] Exécuter `/notif subscribe` pour un sous-produit
- [ ] Poster une annonce correspondant à cet abonnement
- [ ] Vérifier que l’utilisateur reçoit une notification dans le canal, avec mention

### 📋 Liste & désabonnement
- [ ] Exécuter `/notif list` → vérifier présence de l’abonnement
- [ ] Exécuter `/notif unsubscribe ID` → vérifier suppression correcte

---

## ⚙️ Automatisations

### 🔁 Rappel après 3 jours
- [ ] Créer une annonce 
- [ ] Confirmer que l’auteur reçoit un rappel automatique

### 🧹 Suppression après 5 jours
- [ ] Créer une annonce (simuler passage du temps via la db)
- [ ] Vérifier que l’annonce est supprimée automatiquement

---

## 🧪 Résilience & erreurs

### Champs invalides
- [ ] Essayer de créer une annonce avec champ vide ou invalide → message d’erreur attendu

### Suppression invalide
- [ ] Exécuter `/market remove ID` avec un mauvais ID → message d’erreur

### Abonnement invalide
- [ ] Essayer `/notif subscribe` sur un sous-produit inexistant → rejet propre

---

## 📋 Messages & cohérence

- [ ] Les messages d’erreur et de confirmation sont clairs et sans fautes
- [ ] Les comportements correspondent bien au guide utilisateur
- [ ] L’interface est fluide et intuitive

---

## ⏱️ Test de charge rapide

- [ ] Ajouter 20 annonces → vérifier stabilité
- [ ] Créer 5 abonnements à un sous-produit → publier une annonce → vérifier 5 notifs distinctes

