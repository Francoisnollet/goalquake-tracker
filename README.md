# goalquake-tracker
Goal detector that shakes the seismograph. Inspired by the real 'goalquakes' recorded by Belgium's Royal Observatory.

# Red Devil's Goalquake Tracker

Une mini-app pour suivre les buts des Diables Rouges sans regarder le match.

## Le contexte

Je ne pouvais pas voir le match Belgique-Espagne, j'étais à un mariage. J'ai découvert qu'un géologue de l'Observatoire royal de Belgique documente depuis peu les "goalquakes" : les sauts de joie des supporters, au moment des buts, font trembler la terre suffisamment fort pour être enregistrés par le réseau sismique belge.

Du coup l'idée était simple : puisque le sol tremble quand les Diables marquent, autant construire un truc qui me le dise en direct, plutôt que de sortir mon téléphone toutes les cinq minutes pendant la cérémonie.

## Ce que ça fait, concrètement

- Suit le score du match en direct (via l'API publique ESPN)
- Déclenche une alerte visuelle et sonore (façon corne de brume de stade) à chaque but belge
- Garde un relevé complet du match, avec un pic à chaque but
- Un bouton discret en bas pour noter un but manuellement, si jamais l'API de score fait grève au mauvais moment

## Ce que ça ne fait pas

Ça ne mesure aucune vraie donnée sismique en temps réel. Les vrais goalquakes ne sont analysés qu'après coup, à la main, sur le signal brut d'un sismomètre, pas via un flux public qu'on peut interroger pendant le match. Le sismographe animé ici est une mise en scène, reliée à un vrai signal (le score), pas à une mesure sismique instantanée. Disons que c'est plus honnête ainsi.

## Stack

Un seul fichier HTML. Pas de backend, pas de base de données, pas de framework. Juste du JS vanille, l'API ESPN, le Web Audio API pour le son, et le localStorage du navigateur pour ne pas tout perdre au premier rafraîchissement.

---

Une idée d'application vous trotte dans la tête ? [On en parle](https://www.linkedin.com/in/francois-nollet).
