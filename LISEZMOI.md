# geometrie

Formules de géométrie plane pour Fadéra : rectangle, cercle, triangle, distance, polygone.

## Installation

```
fadera paquet installer Faderaseny/geometrie
```

## Utilisation

```
importer "paquets/geometrie/principal" comme g

afficher g.aire_rectangle(4, 3)                  # 12
afficher arrondir(g.aire_cercle(2), 2)           # 12.57
afficher g.hypotenuse(3, 4)                      # 5
afficher g.aire_triangle_cotes(3, 4, 5)          # 6
afficher g.distance({ x: 0, y: 0 }, { x: 3, y: 4 })   # 5

soit terrain = [{ x: 0, y: 0 }, { x: 10, y: 0 }, { x: 10, y: 6 }, { x: 0, y: 6 }]
afficher g.aire_polygone(terrain)                # 60
afficher g.perimetre_polygone(terrain)           # 32
```

## Fonctions

| Fonction | Rôle |
|---|---|
| `aire_rectangle(longueur, largeur)` | aire d'un rectangle |
| `perimetre_rectangle(longueur, largeur)` | périmètre d'un rectangle |
| `aire_cercle(rayon)` | aire d'un cercle |
| `perimetre_cercle(rayon)` | circonférence d'un cercle |
| `aire_triangle(base, hauteur)` | aire d'un triangle |
| `triangle_possible(a, b, c)` | vrai si trois côtés forment un triangle |
| `aire_triangle_cotes(a, b, c)` | aire d'un triangle à partir de ses trois côtés (formule de Héron) |
| `hypotenuse(a, b)` | hypoténuse d'un triangle rectangle |
| `distance(p, q)` | distance entre deux points `{ x, y }` |
| `aire_polygone(points)` | aire d'un polygone simple (liste de points) |
| `perimetre_polygone(points)` | périmètre d'un polygone |

Une valeur négative (longueur, rayon…) déclenche une erreur claire, à rattraper avec `essayer … attraper`.

## Tests

```
fadera tester paquets/geometrie/tests.fa
```

Licence : MIT.
