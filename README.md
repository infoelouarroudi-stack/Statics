# 📊 Cours sur les Quartiles (Statistiques)

## 🧠 Introduction

Les **quartiles** sont des valeurs qui **divisent une série statistique en quatre parties égales**.  
Chaque partie contient **25 %** des données.

On distingue :
- **Q1 (1er quartile)** : sépare les **25 %** des plus petites valeurs.  
- **Q2 (2e quartile)** : correspond à la **médiane** (50 % des valeurs en dessous).  
- **Q3 (3e quartile)** : sépare les **75 %** des plus petites valeurs (ou 25 % des plus grandes).

---

## 📐 Méthode de calcul

### Étape 1 : Trier la série dans l’ordre croissant
Avant tout, il faut **classer les données** du plus petit au plus grand.

### Étape 2 : Calculer la position du quartile

Pour une série **non groupée** (liste de données simples, sans fréquences) :

\[
P(Q_k) = \frac{k (n + 1)}{4}
\]

où :
- \( k \) = 1, 2 ou 3 (selon le quartile),
- \( n \) = nombre total de valeurs.

### Étape 3 : Trouver la valeur correspondante

- Si la position \( P(Q_k) \) est **entière**, on prend la valeur à cette position.
- Si elle n’est **pas entière**, on fait une **interpolation linéaire** :
  
  Exemple : \( P(Q_k) = 3.25 \)
  \[
  Q_k = V_3 + 0.25 (V_4 - V_3)
  \]

---

## 📘 Exemple 1 : Série simple

Soit la série suivante :
> 4, 7, 8, 10, 12, 15, 18, 20

1️⃣ **Trier la série (déjà triée)**  
\( n = 8 \)

2️⃣ **Calcul des positions :**
- \( P(Q_1) = \frac{1(8 + 1)}{4} = 2.25 \)
- \( P(Q_2) = \frac{2(8 + 1)}{4} = 4.5 \)
- \( P(Q_3) = \frac{3(8 + 1)}{4} = 6.75 \)

3️⃣ **Calcul des valeurs :**
- \( Q_1 = 7 + 0.25(8 - 7) = 7.25 \)
- \( Q_2 = 10 + 0.5(12 - 10) = 11 \)
- \( Q_3 = 15 + 0.75(18 - 15) = 17.25 \)

✅ **Résultat final :**
| Quartile | Valeur |
|-----------|--------|
| Q1 | 7.25 |
| Q2 (médiane) | 11 |
| Q3 | 17.25 |

---

## 📗 Exemple 2 : Série avec fréquences

| Valeur (x) | 5 | 10 | 15 | 20 | 25 |
|-------------|---|----|----|----|----|
| Effectif (nᵢ) | 3 | 5 | 4 | 6 | 2 |

1️⃣ Calculer les effectifs cumulés :
| x | nᵢ | Cumulé |
|---|----|---------|
| 5 | 3 | 3 |
| 10 | 5 | 8 |
| 15 | 4 | 12 |
| 20 | 6 | 18 |
| 25 | 2 | 20 |

\( n = 20 \)

2️⃣ Positions :
- \( Q_1 = \frac{1(20 + 1)}{4} = 5.25 \)
- \( Q_2 = \frac{2(20 + 1)}{4} = 10.5 \)
- \( Q_3 = \frac{3(20 + 1)}{4} = 15.75 \)

3️⃣ Recherche dans les cumulés :
- **5.25 →** Q1 est entre 3 et 8 → donc **Q1 = 10**
- **10.5 →** Q2 entre 8 et 12 → donc **Q2 = 15**
- **15.75 →** Q3 entre 12 et 18 → donc **Q3 = 20**

✅ Résultat :
| Quartile | Valeur |
|-----------|--------|
| Q1 | 10 |
| Q2 | 15 |
| Q3 | 20 |

---

## 🧩 Exercices d’application

### 🔹 Exercice 1 (Facile)
Série : 2, 5, 6, 8, 10, 11, 13, 15  

👉 Trouver Q1, Q2 et Q3.

#### ✅ Correction :
\( n = 8 \)

\( P(Q_1) = 2.25 → Q_1 = 5 + 0.25(6-5) = 5.25 \)  
\( P(Q_2) = 4.5 → Q_2 = 8 + 0.5(10-8) = 9 \)  
\( P(Q_3) = 6.75 → Q_3 = 11 + 0.75(13-11) = 12.5 \)

| Quartile | Valeur |
|-----------|--------|
| Q1 | 5.25 |
| Q2 | 9 |
| Q3 | 12.5 |

---

### 🔹 Exercice 2 (Moyen)
Série : 3, 5, 7, 8, 10, 12, 15, 18, 20, 25  

👉 Calculer Q1, Q2, Q3.

#### ✅ Correction :
\( n = 10 \)

\( P(Q_1) = 2.75 → Q_1 = 5 + 0.75(7-5) = 6.5 \)  
\( P(Q_2) = 5.5 → Q_2 = 8 + 0.5(10-8) = 9 \)  
\( P(Q_3) = 8.25 → Q_3 = 15 + 0.25(18-15) = 15.75 \)

| Quartile | Valeur |
|-----------|--------|
| Q1 | 6.5 |
| Q2 | 9 |
| Q3 | 15.75 |

---

### 🔹 Exercice 3 (Difficile — avec fréquences)

| Valeur (x) | 10 | 20 | 30 | 40 | 50 |
|-------------|----|----|----|----|----|
| Effectif (nᵢ) | 2 | 3 | 5 | 4 | 6 |

👉 Trouver Q1, Q2 et Q3.

#### ✅ Correction :
1️⃣ Cumulés :
| x | nᵢ | Cumulé |
|---|----|---------|
| 10 | 2 | 2 |
| 20 | 3 | 5 |
| 30 | 5 | 10 |
| 40 | 4 | 14 |
| 50 | 6 | 20 |

\( n = 20 \)

2️⃣ Positions :
- Q1 = 5.25 → entre 5 et 10 → **x = 30**
- Q2 = 10.5 → entre 10 et 14 → **x = 40**
- Q3 = 15.75 → entre 14 et 20 → **x = 50**

✅ Résultat final :
| Quartile | Valeur |
|-----------|--------|
| Q1 | 30 |
| Q2 | 40 |
| Q3 | 50 |

---

## 🧾 Résumé

| Quartile | Signification | Pourcentage |
|-----------|----------------|--------------|
| Q1 | 25 % des valeurs inférieures | 25 % |
| Q2 | Médiane (50 %) | 50 % |
| Q3 | 75 % des valeurs inférieures | 75 % |

---

## 💡 Astuce
🔸 Si la série est longue, tu peux utiliser **Excel**, **Python (numpy.percentile)** ou **calculatrice scientifique** pour vérifier tes résultats.  
🔸 Toujours **trier la série** avant de calculer !

---

© Monir EL OUARROUDI – Cours interactif de statistiques 📈



# Correction complète — Histogramme et indicateurs statistiques
Collège Saint Charles — Classe de Troisième  
(Exercice : répartition des notes pour 30 élèves)

---

## Données (issues de l’histogramme)
Les classes de notes et leurs effectifs sont :

| Classe de notes | Effectif |
|-----------------|----------|
| De 0 à 3        | 5        |
| De 4 à 7        | 6        |
| De 8 à 11       | 7        |
| De 12 à 15      | 6        |
| De 16 à 20      | 6        |
| **Total**       | **30**   |

Cumulés (effectifs cumulés) :  
5 ; 5+6 = 11 ; 11+7 = 18 ; 18+6 = 24 ; 24+6 = 30.

---

## 1) Explication — comment compléter le tableau à partir de l’histogramme

- Pour chaque barre de l’histogramme, on lit la **hauteur** de la barre : elle donne l’**effectif** (le nombre d’élèves) qui ont une note dans l’intervalle correspondant.  
- On reporte cet effectif dans la ligne de la classe correspondante.  
- On additionne ensuite tous les effectifs pour obtenir le total (ici 30).  

Exemple (lecture) :
- Barres pour 0–3 → effectif = 5  
- Barres pour 4–7 → effectif = 6  
- etc.

---

## 2) Quelle(s) valeur(s) peuvent correspondre à la valeur exacte de la moyenne ?

**Rappel utile** : la moyenne arithmétique exacte vaut la somme des notes divisée par 30.  
Comme le professeur ne met que des **notes entières**, la somme des 30 notes est un entier. Donc la moyenne exacte est un nombre de la forme **(entier) ÷ 30**.

### Bornes possibles de la moyenne
Pour savoir quelles valeurs sont possibles il est utile de calculer la **minimum** et la **maximum** possibles de la somme (et donc de la moyenne), compte tenu des classes :

- Pour obtenir la somme minimale, on prend **la borne inférieure** de chaque classe pour chaque élève de la classe :
  \[
  S_{\min} = 5\times 0 + 6\times 4 + 7\times 8 + 6\times 12 + 6\times 16 = 248
  \]
  Moyenne minimale possible : \( \dfrac{248}{30} \approx 8{,}266\).

- Pour obtenir la somme maximale, on prend **la borne supérieure** de chaque classe :
  \[
  S_{\max} = 5\times 3 + 6\times 7 + 7\times 11 + 6\times 15 + 6\times 20 = 344
  \]
  Moyenne maximale possible : \( \dfrac{344}{30} \approx 11{,}466\).

Donc la moyenne exacte doit être comprise entre **≈ 8,266** et **≈ 11,466**, et en plus elle doit être de la forme \( \dfrac{k}{30}\) avec \(k\) entier (puisque toutes les notes sont entières).

### Vérification des quatre nombres proposés
Les nombres proposés sont : **7,7 ; 10,9 ; 10 ; 10,35**.

- 7,7 → \(7{,}7 \times 30 = 231\). 231 < 248 → **impossible** (en dehors des bornes).
- 10,9 → \(10{,}9 \times 30 = 327\). 327 est un entier et 248 ≤ 327 ≤ 344 → **possible**.
- 10 → \(10 \times 30 = 300\). 300 est un entier et 248 ≤ 300 ≤ 344 → **possible**.
- 10,35 → \(10{,}35 \times 30 = 310{,}5\) → pas un entier (310,5) → **impossible** car la somme des notes doit être un entier.

**Réponse Q2 :** Parmi les quatre nombres, **10,9** et **10** peuvent correspondre à la moyenne exacte (justification ci-dessus). Les deux autres sont impossibles (7,7 trop petit ; 10,35 non entier une fois multiplié par 30).

---

## 3) Que peut-on dire de l'étendue (max − min) des notes de la classe ?

- La plus petite note possible est située **dans la classe 0–3** → valeur comprise entre 0 et 3.  
- La plus grande note possible est située **dans la classe 16–20** → valeur comprise entre 16 et 20.

Donc l’étendue \(E = \text{max} - \text{min}\) est comprise entre :
\[
\min(E) = 16 - 3 = 13 \quad\text{et}\quad \max(E) = 20 - 0 = 20.
\]

On peut donc affirmer que **l’étendue est un entier compris entre 13 et 20**. (On ne peut pas être plus précis sans connaître les valeurs exactes.)

---

## 4) Que peut-on dire de la médiane ?

Rappel : pour une série de taille \(n = 30\) (pair), la médiane est la moyenne entre la **15ᵉ** et la **16ᵉ** valeur (les valeurs rangées en ordre croissant).

Regardons les effectifs cumulés :
- Jusqu’à la classe 0–3 : 5 valeurs (positions 1 à 5)  
- Jusqu’à la classe 4–7 : 11 valeurs (positions 1 à 11)  
- Jusqu’à la classe 8–11 : 18 valeurs (positions 1 à 18)

Les positions **15** et **16** se trouvent donc **dans la classe 8–11** (car la classe 8–11 couvre les positions 12 à 18).

Conclusion :
- Les 15ᵉ et 16ᵉ valeurs sont comprises entre **8 et 11**.  
- La médiane (moyenne des 15ᵉ et 16ᵉ) est donc comprise entre **8** et **11**.  
- Comme les notes sont entières, la médiane peut prendre des valeurs entières ou demi-entiers (par exemple 8, 8,5, 9, …, 11) selon les valeurs exactes des 15ᵉ et 16ᵉ.  
- On peut préciser que **la médiane ∈ [8 ; 11]**, mais on ne peut pas donner la valeur exacte sans la liste détaillée des notes.

---

## 5) Construire une série de 30 notes entières (0–20) qui respecte :
- la répartition indiquée par l’histogramme (effectifs par classe ci-dessus) ;
- **la moyenne exactement 10** ;
- **l’étendue = 15** ;
- la note **8** peut être considérée comme note médiane.

### Méthode et construction
- Moyenne = 10 pour 30 élèves implique somme totale = \(30 \times 10 = 300\).
- Nous devons construire 30 entiers répartis en : 5 (0–3), 6 (4–7), 7 (8–11), 6 (12–15), 6 (16–20).
- L’étendue doit valoir 15 → choisir par exemple minimum = 2 (dans 0–3) et maximum = 17 (dans 16–20), alors étendue = 17 − 2 = 15.
- Pour que 8 soit la médiane, on veut que les 15ᵉ et 16ᵉ valeurs soient 8 (ou leur moyenne = 8). Puisque la classe 8–11 contient les positions 12 à 18, on peut faire en sorte que plusieurs valeurs de la classe 8–11 soient égales à 8 ; ainsi la moyenne des 15ᵉ et 16ᵉ sera 8.

Une solution simple (toutes les valeurs d’une même classe égales à une valeur représentative) :

- Classe 0–3 (5 élèves) → tous **2**  
- Classe 4–7 (6 élèves) → tous **7**  
- Classe 8–11 (7 élèves) → tous **8** (assure que 15ᵉ et 16ᵉ sont 8 → médiane = 8)  
- Classe 12–15 (6 élèves) → tous **15**  
- Classe 16–20 (6 élèves) → tous **17**

Vérification :
- Effectifs corrects : 5, 6, 7, 6, 6 → total 30.  
- Somme : \(5\times2 + 6\times7 + 7\times8 + 6\times15 + 6\times17\)  
  \(= 10 + 42 + 56 + 90 + 102 = 300\). Moyenne = \(300/30 = 10\).  
- Étendue = max − min = 17 − 2 = **15**.  
- Médiane : positions 15 et 16 sont dans la classe 8–11 et valent 8 → médiane = (8+8)/2 = **8**.

Série possible (liste de 30 notes) :
2,2,2,2,2, (5 fois)
7,7,7,7,7,7, (6 fois)
8,8,8,8,8,8,8,(7 fois)
15,15,15,15,15,15, (6 fois)
17,17,17,17,17,17 (6 fois)
On peut évidemment donner les valeurs dans un autre ordre (la série doit être triée pour lire médiane), mais cette liste respecte toutes les contraintes.

