Rapport d'activité
==================

Un rapport d'activité permet d'enregistrer des informations durant l'exécution du code à différents niveaux. C'est-à-dire que l'on peut enregistrer tout ce qui se passe, le déroulement du programme et ainsi mieux comprendre ce qu'il se passe. Les niveaux sont une façon de dissocier les simples messages d'information des messages d'erreurs en passant par les alertes.

## Implémentation

Le rapport d'activités de Beluga est un objet contenant seulement des méthodes statiques. Il existe une méthode pour afficher le contenu du log ainsi que plusieurs méthodes permettant l'enregistrement d'un message.

Ci-dessous la liste des méthodes permettant d'enregistrer un message :

 * `public static function warn(msg : String)` : Enregistre un message d'alerte.
 * `public static function error(msg : String)` : Enregitre un message d'erreur.
 * `public static function info(msg : String)` : Enregistre un message d'information.
 * `public static function debug(msg : String)` : Enregistre un message de débogage.

### Exemple

Voici comment nous pouvons utiliser les rapports d'activité :

```haxe
	Log.warn("Message d'alerte");
	Log.flush(); //Écrit une ligne contenant "Message d'alerte"
```

## Limitations

La version actuelle du Log ne permet pas de filtrer les niveaux des logs à afficher. Normalement, on devrait pouvoir par exemple ignorer les messages peu important d'information si l'on rencontre un bug critique.