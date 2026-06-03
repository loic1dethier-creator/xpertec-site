# 🎙️ Agent Vocal IA (pour iPhone)

Un assistant vocal personnel : vous **parlez**, une IA (**Claude**) comprend, **répond à voix haute** et peut **agir sur votre iPhone** (appels, SMS, e-mails, itinéraires, ouverture d'apps, et **Raccourcis Apple**).

C'est une **web-app** : rien à compiler, pas de serveur. Elle fonctionne dans Safari et s'ajoute à l'écran d'accueil comme une vraie app.

---

## ⚠️ À lire d'abord : ce qu'un iPhone autorise (et pas)

Apple **interdit** à toute app/page web de « prendre le contrôle total » du téléphone (taper sur l'écran à votre place, piloter n'importe quelle app). C'est le *sandbox* iOS, infranchissable sans jailbreak.

Ce que cet agent **peut** réellement faire, via les mécanismes officiels d'iOS :

- 📞 **Appeler** un numéro
- 💬 **Préparer un SMS** (vous confirmez l'envoi)
- ✉️ **Préparer un e-mail**
- 🗺️ **Ouvrir un itinéraire** dans Plans
- 📲 **Ouvrir une app ou un site**
- ⚡️ **Lancer un Raccourci Apple** → *c'est ici que tout devient possible*

> Pour un contrôle **total** du téléphone à la voix sans IA, activez aussi le **Contrôle Vocal** natif : Réglages → Accessibilité → Contrôle Vocal. Les deux sont complémentaires.

---

## 🚀 Installation (3 minutes)

1. **Mettez le site en ligne** (GitHub Pages recommandé) :
   - Dépôt → *Settings* → *Pages* → Source : branche `main` (ou votre branche), dossier `/ (root)`.
   - L'app sera sur `https://<vous>.github.io/xpertec-site/voice-agent/`.
   - ⚠️ HTTPS est **obligatoire** pour le micro (GitHub Pages le fournit).

2. **Ouvrez l'URL dans Safari** sur l'iPhone.

3. **Ajoutez à l'écran d'accueil** : bouton Partager → *Sur l'écran d'accueil*. Vous avez maintenant une icône d'app en plein écran.

4. **Clé API Claude** : ouvrez ⚙️ → collez votre clé (depuis
   [console.anthropic.com](https://console.anthropic.com/settings/keys)) → *Enregistrer*.
   La clé reste **uniquement sur votre iPhone** (localStorage).

5. **Parlez** : appuyez sur le gros micro 🎙️, parlez, re-appuyez pour arrêter.

---

## 🧠 Donner plus de pouvoir à l'agent (Raccourcis)

L'outil `lancer_raccourci` permet à l'IA de déclencher **n'importe quel Raccourci** que vous créez dans l'app **Raccourcis** d'Apple. Exemples :

- Un Raccourci « Lumière salon » → l'agent l'allume quand vous dites « allume le salon ».
- Un Raccourci « Note rapide » qui reçoit du texte → « note que je dois rappeler le client ».
- Un Raccourci « Maison » HomeKit, « Mode nuit », « Lancer ma playlist », etc.

L'agent appelle le Raccourci **par son nom exact** et peut lui passer du texte. Créez vos Raccourcis, dites leur nom à l'agent, et il les déclenchera.

---

## ⚙️ Réglages disponibles

| Réglage | Rôle |
|---|---|
| **Clé API** | Active l'IA Claude (sans clé : mode dictée). |
| **Modèle** | Haiku (rapide, idéal voix) · Sonnet (équilibré) · Opus (le plus intelligent). |
| **Langue** | Langue de reconnaissance vocale + voix de réponse. |
| **Personnalité** | Instructions données à l'agent (rôle, ton, règles). |
| **Voix haute** | Active/coupe la lecture des réponses. |
| **Écoute continue** | Mode mains libres : ré-écoute après chaque réponse. |

---

## 🔒 Confidentialité & sécurité

- La clé API est stockée **sur l'appareil uniquement** et envoyée **directement** à l'API d'Anthropic (aucun serveur intermédiaire).
- N'utilisez cette page que sur **votre appareil personnel**.
- L'usage de l'API Claude est **facturé à la consommation** par Anthropic.

## 📱 Compatibilité

- **iPhone / Safari** : recommandé (reconnaissance + synthèse vocale OK).
- Chrome/Edge desktop : fonctionne aussi.
- La reconnaissance vocale utilise l'API Web Speech native du navigateur.
