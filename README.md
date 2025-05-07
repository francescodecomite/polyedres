# polyedres
 propriétés des polyèdres (platoniciens, archimédiens, de Catalan, de Johnson)

Ce répertoire contient les données géométriques permettant de construire les polyèdres platoniciens, archimédiens, polyèdres de Catalan et polyèdres de Johnson. 
J'ai récupéré çà à il y a très longtemps sur Internet et je ne me rappelle plus la source (qui a l'air de ne plus exister, la recherche ne donne rien dans Google)

Chaque fichier porte le nom du polyèdre qu'il représente. 

Les fichiers au fomat OFF (https://en.wikipedia.org/wiki/OFF_(file_format)) sont en ASCII et se décomposent comme suit : 


1. Les deux premières lignes sont des commentaires.  
2. La troisième ligne comprend trois chiffres : le nombre de sommets, de faces et d'arêtes du solide ('S','F','A')
3. Les 'S' lignes suivantes sont les coordonnées 3D de chaque sommet. L'ordre dans lequel sont donnés ces sommets leur donne un numéro d'ordre commençant à 0
4. Les 'F' lignes suivantes définissent les faces. Pour chaque ligne, le premier nombre indique le nombre 'N' de cotés de cette face. Les 'N' chiffres suivants sont les index de
sommets utilisés pour cette face. 
5. Les 'A' lignes finales définissent les arêtes en utilisant les index des sommets qui définissent l'arête. 


Exemple : le cube

# Cube (Hexahedron)
# Data: Exact Mathematics
8 6 12                                  -------------> 8 sommets, 6 faces, 12 arêtes
 1    1    1                            -------------> Les coordonnées des 8 sommets
 1    1   -1
 1   -1    1
 1   -1   -1
-1    1    1
-1    1   -1
-1   -1    1
-1   -1   -1
4 6 4 0 2                                 ----------> La première face a quatre cotés, les sommets sonts le 6ème, suivi du 4ème, du zérotième et du deuxième
4 5 1 0 4
4 7 5 4 6
4 1 3 2 0
4 3 7 6 2
4 7 3 1 5
0 1                                       --------------> les arêtes
0 2
0 4
1 3
1 5
2 3
2 6
3 7
4 5
4 6
5 7
6 7
