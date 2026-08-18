# bot-TS1

Ancien prototype de bot Discord en JavaScript, conservé comme petit exercice autour de **Node.js** et de **discord.js**.

Le comportement versionné est volontairement minimal : le bot écoute les messages et répond `pong` lorsqu'il reçoit `ping`.

> **Projet legacy :** ce dépôt utilise une ancienne API de discord.js et ne doit pas être pris comme modèle de bot Discord moderne.

## Sécurité

Ne placez jamais un token Discord directement dans le code source.

Si un token a déjà été commité publiquement, considérez-le comme compromis : **révoquez-le dans le portail Discord Developer**, générez-en un nouveau et utilisez une variable d'environnement.

Exemple :

```env
DISCORD_TOKEN=replace_me
```

Puis chargez cette variable côté Node.js au lieu d'écrire le secret dans `main.js`.

## Installation

```bash
git clone https://github.com/LeoPonchon/bot-TS1.git
cd bot-TS1
yarn install
```

ou, selon le lockfile et votre environnement :

```bash
npm install
```

## Lancement

Après avoir adapté le code pour lire `DISCORD_TOKEN` depuis l'environnement :

```bash
node main.js
```

## Ce que montre ce dépôt

- création d'un client Discord ;
- écoute des messages ;
- réponse à une commande textuelle simple ;
- base d'un bot événementiel Node.js.

Pour un nouveau projet, partez plutôt sur une version actuelle de discord.js et sur les intents/commandes slash recommandés par Discord.
