# FredbearCoop

**Play _Those Nights at Fredbear's_ in co-op (2 players).**
**Jouer à _Those Nights at Fredbear's_ en coop (2 joueurs).**

> Experimental fan-made mod. All credit for the game goes to its original creator.
> Mod expérimental fait par un fan. Tout le mérite du jeu revient à son créateur original.

What it does:
- See your friend in your game as a grey ghost with a green light.
- The animatronics, battery, time and doors follow the host's game.

[🇫🇷 Version française plus bas](#-français)

---

## 🇬🇧 English

### 1. Install (on both PCs)
1. **The game**: *Those Nights at Fredbear's*, free on **GameJolt**.
2. **UE4SS**: on GitHub, search for **RE-UE4SS**, open **Releases** and download the zip. Unzip it into `TNAF_ND\Binaries\Win64`.
3. **Python**: get it from [python.org](https://www.python.org/downloads/). ⚠️ Tick **"Add python.exe to PATH"** during setup.
4. **Radmin VPN** (free). One player creates a network, and the other joins it.

### 2. Install the mod (on both PCs)
1. Download the zip from **Releases** and unzip it.
2. Copy the **FredbearCoop** folder into `Win64\ue4ss\Mods`.
   The path must be exactly `Mods\FredbearCoop\Scripts\main.lua`.
3. Copy **relay.py** into `Win64\ue4ss\Mods`.
4. Open `Mods\mods.txt`:
   - add `FredbearCoop : 1`
   - set `SplitScreenMod : 0` and `LineTraceMod : 0`

### 3. Edit `config.lua`
Open `Mods\FredbearCoop\Scripts\config.lua` with Notepad.

**Host:** change nothing.
```lua
ROLE = "host",
```
**Other player:** change these 2 lines.
```lua
ROLE = "client",
HOST_IP = "26.xx.xx.xx",
```
`26.xx.xx.xx` = the host's Radmin IP (the number starting with 26 in Radmin VPN). Keep the quotes and the comma.

### 4. Play
1. In the `Win64\ue4ss\Mods` folder, click the address bar, type `cmd` and press Enter.
2. Type this, with **the OTHER player's IP**:
   ```
   py relay.py 26.xx.xx.xx
   ```
3. Keep that window open for the whole game.
4. Both players launch the game and start **the same night**. After about 15 seconds, the relay says `Connecté !`.

**Keys:** `F3` shows the ghost in front of you for 4 seconds, to test it. `F4` hides or shows the ghost.

### Troubleshooting
| Problem | Fix |
|---|---|
| `Python was not found` | Use `py` instead of `python`, or reinstall Python with "Add to PATH". |
| `WinError 10048` | A relay is already running. Close all black windows and start it again. |
| Game crashes at launch | Check that `SplitScreenMod : 0` is set in mods.txt. |
| You don't see each other | Check the IPs: each player types the **other** player's IP in the relay, and the client puts the host's IP in config.lua. |
| Weak PC | In config.lua, set `TICK_MS = 100,` and `DISCOVER_S = 15,`. Lower the graphics. |

---

## 🇫🇷 Français

### 1. À installer (sur les 2 PC)
1. **Le jeu** : *Those Nights at Fredbear's*, gratuit sur **GameJolt**.
2. **UE4SS** : sur GitHub, cherche **RE-UE4SS**, ouvre **Releases** et télécharge le zip. Dézippe-le dans `TNAF_ND\Binaries\Win64`.
3. **Python** : sur [python.org](https://www.python.org/downloads/). ⚠️ Coche **« Add python.exe to PATH »** pendant l'installation.
4. **Radmin VPN** (gratuit). Un joueur crée un réseau, l'autre le rejoint.

### 2. Installer le mod (sur les 2 PC)
1. Télécharge le zip dans **Releases** et dézippe-le.
2. Copie le dossier **FredbearCoop** dans `Win64\ue4ss\Mods`.
   Le chemin doit être exactement `Mods\FredbearCoop\Scripts\main.lua`.
3. Copie **relay.py** dans `Win64\ue4ss\Mods`.
4. Ouvre `Mods\mods.txt` :
   - ajoute `FredbearCoop : 1`
   - mets `SplitScreenMod : 0` et `LineTraceMod : 0`

### 3. Régler `config.lua`
Ouvre `Mods\FredbearCoop\Scripts\config.lua` avec le Bloc-notes.

**L'hôte :** ne change rien.
```lua
ROLE = "host",
```
**L'autre joueur :** change ces 2 lignes.
```lua
ROLE = "client",
HOST_IP = "26.xx.xx.xx",
```
`26.xx.xx.xx` = l'IP Radmin de l'hôte (le numéro qui commence par 26 dans Radmin VPN). Garde les guillemets et la virgule.

### 4. Jouer
1. Dans le dossier `Win64\ue4ss\Mods`, clique dans la barre d'adresse, tape `cmd` et appuie sur Entrée.
2. Tape ceci, avec **l'IP de l'AUTRE joueur** :
   ```
   py relay.py 26.xx.xx.xx
   ```
3. Laisse cette fenêtre ouverte pendant toute la partie.
4. Lancez le jeu tous les deux et commencez **la même nuit**. Au bout de 15 secondes environ, le relais affiche `Connecté !`.

**Touches :** `F3` affiche le fantôme devant toi pendant 4 secondes, pour tester. `F4` cache ou montre le fantôme.

### Problèmes courants
| Problème | Solution |
|---|---|
| `Python was not found` | Utilise `py` au lieu de `python`, ou réinstalle Python en cochant « Add to PATH ». |
| `WinError 10048` | Un relais tourne déjà. Ferme toutes les fenêtres noires et relance-le. |
| Le jeu crashe au lancement | Vérifie que `SplitScreenMod : 0` est bien dans mods.txt. |
| On ne se voit pas | Vérifie les IP : chacun tape l'IP de l'**autre** dans le relais, et le client met celle de l'hôte dans config.lua. |
| PC faible | Dans config.lua, mets `TICK_MS = 100,` et `DISCOVER_S = 15,`. Baisse les graphismes. |


c'est mon premier projet alors soyez indulgent please
