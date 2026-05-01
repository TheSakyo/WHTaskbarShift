# Taskbar Monitor Switcher

> **Fork** de [Primary taskbar on secondary monitor](https://windhawk.net/mods/taskbar-primary-on-secondary-monitor) 
> par **m417z**.
> </br>
> Toutes les fonctionnalités d'origine sont conservées ; un **raccourci clavier** a été ajouté.
>
> 📂 **Inclus dans [Windhawk Mods Collection](https://github.com/TheSakyo/windhawk-mods)**

Déplace la barre des tâches principale — y compris les icônes de zone de notification,
les notifications, le centre d’action, etc. — vers un autre écran.

L’écran actif peut être changé de trois façons :
- **Paramètres** — choisir un écran par numéro ou nom d’interface (toutes versions).
- **Clic** — double-clic ou clic molette sur une zone vide de la barre des tâches (Windows 11 uniquement).
- **Raccourci clavier** — appuyez sur un raccourci configurable pour déplacer
instantanément la barre des tâches vers l’écran où se trouve le curseur.

![Demonstration](https://i.imgur.com/hFU9oyK.gif)

## Sélection d’un écran

### Par numéro d’écran

Définissez le paramètre **Monitor** sur le numéro souhaité (1, 2, 3 …). Notez
que ce numéro peut différer de celui affiché dans les paramètres d’affichage Windows.

### Par nom d’interface

Si les numéros d’écran changent fréquemment (par exemple après verrouillage du PC
ou redémarrage), utilisez plutôt le nom d’interface du moniteur :

1. Ouvrez l’onglet **Advanced** du mod.
2. Réglez **Debug logging** sur **Mod logs**.
3. Cliquez sur **Show log output**.
4. Entrez n’importe quel texte (ex. `TEST`) dans le champ **Monitor interface name** puis sauvegardez.
5. Dans le journal, cherchez des lignes comme :

```txt
Found display device \\.\DISPLAY1, interface name: \\?\DISPLAY#DELA1D2#5&abc123#0#{e6f07b5f-…}
Found display device \\.\DISPLAY2, interface name: \\?\DISPLAY#GSM5B09#4&def456#0#{e6f07b5f-…}
```

6. Copiez le nom d’interface correspondant (ou une sous-partie unique) dans
**Monitor interface name**.
7. Remettez **Debug logging** sur **None** une fois terminé.

**Monitor interface name** est prioritaire sur le numéro **Monitor** lorsque les
deux sont définis.

## Raccourci clavier

Lorsqu’un raccourci clavier est configuré, l’appuyer déplace la barre des tâches
principale vers l’écran situé sous le curseur. Si le curseur est **déjà sur
l’écran de la barre active**, le raccourci est ignoré silencieusement — aucun
déplacement involontaire.
