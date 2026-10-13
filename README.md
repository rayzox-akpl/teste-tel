# Hub

Hub de scripts avec interrupteurs. Il marche sur PC (Solara, Xeno) et sur téléphone (Delta).

## Lancer le hub

Colle cette ligne dans ton executor, en remplaçant `PSEUDO/DEPOT` par ton dépôt :

```lua
loadstring(game:HttpGet("https://raw.githubusercontent.com/PSEUDO/DEPOT/main/hub.lua?v=" .. tostring(os.time())))()
```

Le `?v=` sert d'anti-cache : tu récupères toujours la dernière version poussée.
Après un changement de serveur, le hub se relance tout seul et rallume les scripts que tu avais activés.

**Important :** dans `hub.lua`, change aussi la ligne `local GITHUB = "rayzox-akpl/teste"` pour mettre le même `PSEUDO/DEPOT`.

## Scripts

| Interrupteur | Fichier | Ce qu'il fait |
|---|---|---|
| Kronax | `h_kronax.lua` | Boss Kronax, ancienne version |
| KronaxMinigun | `kronax_minigun.lua` | Kronax au minigun, avec Start, Skip et Retry automatiques. Ne s'active que dans le raid Kronax |
| LunosMinigun | `lunos_minigun.lua` | Lunos au minigun, avec Start, Skip et Retry automatiques. Ne s'active que dans le raid Lunos |
| Invaded | `farm_invaded.lua` | Donjon envahi : rituel, puis cristaux, puis mobs. Ne s'active que dans un donjon envahi |
| FarmInfinite | `farm_infinite.lua` | Farm infinite (april fools) |
| TpLunars | `tp_lunars.lua` | Farm en TP + Lunar Shard |

Kronax et KronaxMinigun ne peuvent pas être allumés en même temps : allumer l'un éteint l'autre. Pareil pour Invaded et FarmInfinite.

## Commandes

- **B** : arrête KronaxMinigun, LunosMinigun et Invaded.
- **RightCtrl** (PC) : cache ou affiche le hub.
- **Bouton rond HUB** (téléphone) : ouvre ou ferme le hub. Tu peux le déplacer en le faisant glisser avec le doigt.
- Le hub disparaît tout seul pendant les écrans Start et Retry, pour ne pas gêner les clics automatiques.
