# 🕵️‍♂️ Red Notice [425] (14 solves)

> **Catégorie :** OSINT  
> **Difficulté :** Moyen  
> **Auteur :** migattenochauvui

---

<img src="https://raw.githubusercontent.com/Raytoou/nbctf/main/osint/images/wanted.jpg" alt="Image" width="300" style="display:block;margin:auto"/>

---

## 🧩 1. Enoncé

Le challenge nous demande d'identifier une personne et d'y trouver les informations ci-dessous à partir de l'image envoyée précédemment :

- Sa **nationalité**  
- Sa **taille** en centimètres  
- Un **média** le mentionne en 2018, il faut retrouver **la propriétaire du site** de ce média en **2005**

Il nous est d'ailleurs précisé que la publication du média est sur un réseau social très connu en 2018.

**Format attendu :**  
`NBCTF{Pays_Taille en cm_Prenom-Nom}`  
Exemple → `NBCTF{Chine_181_Carine-Dupont}`



## 🔍 2. Recherche inversée

En faisant une recherche inversée via l'image qui nous est donnée, j'accède à de multiples sites qui présentent l'individu sur la photo il s'appellerait **Aram Kohnepushi**. Une fois le nom/prénom trouvé, la première chose qui me vient en tête est donc de faire du dork.



## 🌐 3. Dork

J'utilise Google pour effectuer une recherche telle que : `"Aram Kohnepushi"`.  
Cette recherche me mène vers un site nommé **Offender Warning** qui présente les caractéristiques des personnes recherchées la fiche d'Aram indique qu'il est **Iranien** et qu'il fait **1,74 m** (soit **174 cm**).

---

<img src="https://raw.githubusercontent.com/Raytoou/nbctf/main/osint/images/dork.png" width="1000" style="display:block;margin:auto"/>
<img src="https://raw.githubusercontent.com/Raytoou/nbctf/main/osint/images/height.png"  width="600" style="display:block;margin:auto"/>

---

## 🧠 4. Retrouver le média

Maintenant qu'on possède son nom, sa taille et sa nationalité, il nous manque le média qui mentionne Aram en 2018.  
L'énoncé précise que la publication du média est sur un réseau social très connu en 2018. J'avais d'abord pensé à Facebook, mais en 2018 **Twitter** avait déjà pris l'ascendant sur Facebook ; je décide donc de chercher sur Twitter.  
Je trouve un post d'un média mi-2018 qui mentionne Aram et renvoie vers le site `https://www.finn-land.net/`. Le nom de domaine n'est plus détenu aujourd'hui, donc le site n'existe plus.



## 🏁 5. Retrouver le propriétaire malgré le site disparu

Le site n'existe plus, donc j'utilise Wayback Machine pour restaurer le site en 2005 et voir ce qu'il contenait.  
Sur l'archive de 2005, le propriétaire du site est indiqué dans le copyright tel que : © Cornelia Kiaupa.


---
