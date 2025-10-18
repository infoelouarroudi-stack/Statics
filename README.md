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

## Données (issues de l’histogramme — table fournie)
Les classes de notes et leurs effectifs sont :

| Classe de notes | Effectif |
|-----------------|----------|
| De 0 à 3        | 5        |
| De 4 à 7        | 6        |
| De 8 à 11       | 9        |
| De 12 à 15      | 6        |
| De 16 à 20      | 4        |
| **Total**       | **30**   |

Effectifs cumulés :  
- Jusqu’à 3 : 5  
- Jusqu’à 7 : 5 + 6 = 11  
- Jusqu’à 11 : 11 + 9 = 20  
- Jusqu’à 15 : 20 + 6 = 26  
- Jusqu’à 20 : 26 + 4 = 30

---

## 1) Explication — comment compléter le tableau à partir de l’histogramme

- Pour chaque intervalle (classe) sur l’histogramme, on lit la **hauteur** de la barre : c’est l’**effectif** d’élèves qui ont une note dans cet intervalle.  
- On inscrit cet effectif dans la table correspondante, puis on additionne pour obtenir le total (ici 30).  
- On calcule aussi les **effectifs cumulés** (utile pour la médiane et les quartiles).

---

## 2) Quels nombres parmi une liste peuvent correspondre à la moyenne exacte ?

**Rappel** : la moyenne arithmétique exacte vaut la somme des 30 notes divisée par 30. Comme les notes sont **entières**, la somme est un entier ; la moyenne exacte est donc de la forme \( \dfrac{K}{30}\) avec \(K\) entier.

Pour savoir quelles valeurs sont possibles, on peut calculer les **bornes** de la somme (en prenant les bornes des classes) :

- **Somme minimale possible** (prendre la borne basse de chaque classe pour tous les élèves) :
  \[
  S_{\min} = 5\times 0 + 6\times 4 + 9\times 8 + 6\times 12 + 4\times 16 = 232.
  \]
  Moyenne minimale possible : \(232/30 \approx 7{,}7333\).

- **Somme maximale possible** (prendre la borne haute de chaque classe) :
  \[
  S_{\max} = 5\times 3 + 6\times 7 + 9\times 11 + 6\times 15 + 4\times 20 = 326.
  \]
  Moyenne maximale possible : \(326/30 \approx 10{,}8667\).

Donc la moyenne exacte doit être comprise entre **≈ 7,7333 et ≈ 10,8667**, et de la forme \(K/30\).

> **Conclusion** : tout nombre proposé doit être dans cet intervalle et être égal à un entier divisé par 30 pour être possible.

*(Si on a une liste précise de valeurs proposées, on vérifie ces deux conditions : 1) dans l’intervalle, 2) multiplié par 30 donne un entier.)*

---

## 3) Que peut-on dire de l’étendue (max − min) ?

- La plus petite note appartient à la classe **0–3** → min ∈ [0 ; 3].  
- La plus grande note appartient à la classe **16–20** → max ∈ [16 ; 20].

Donc l’étendue \(E = \text{max} - \text{min}\) est comprise entre :
\[
\min(E) = 16 - 3 = 13 \quad\text{et}\quad \max(E) = 20 - 0 = 20.
\]
**Réponse Q3 :** l’étendue est un entier **compris entre 13 et 20**. On ne peut pas être plus précis sans les notes individuelles.

---

## 4) Que peut-on dire de la médiane ?

- Il y a \(n = 30\) valeurs (paires). La médiane est la moyenne des **15ᵉ** et **16ᵉ** valeurs (dans la série triée).
- D’après les effectifs cumulés : les positions 12 à 20 appartiennent à la **classe 8–11** (car cumulés jusqu’à 11 → 20).
- Les positions 15 et 16 sont donc **dans la classe 8–11**.

**Conclusion Q4 :** la médiane est comprise entre **8 et 11**. Plus précisément, la moyenne des 15ᵉ et 16ᵉ valeurs (chacune dans [8,11]) donne une médiane ∈ [8 ; 11]. Sans les valeurs exactes, on ne peut pas donner la valeur précise, seulement cette intervalle. Si les 15ᵉ et 16ᵉ sont toutes deux 8, la médiane vaut 8, etc.

---

## 5) Construire une série de 30 notes entières (0–20) qui respecte :
- la répartition indiquée par l’histogramme (effectifs : 5, 6, 9, 6, 4) ;  
- la **moyenne = 10** (donc somme totale = \(30 \times 10 = 300\)) ;  
- l’**étendue = 15** ;  
- la note **8** peut être considérée comme **médiane** (c’est-à-dire la moyenne des 15ᵉ et 16ᵉ vaut 8).

### Méthode
- On choisit des valeurs entières pour chaque classe, en respectant le nombre d’élèves par classe.
- Pour l’étendue = 15 on choisit un **min** dans [0,3] et un **max** dans [16,20] tels que **max − min = 15**. Les possibilités :  
  (min, max) ∈ { (1,16), (2,17), (3,18) }.
- Pour que 8 soit médiane, il faut que les **15ᵉ** et **16ᵉ** valeurs (dans l’ordre) valent 8.  
  Comme les 11 premières valeurs sont ≤7 (effectif cumulé = 11), la **classe 8–11** contient les positions 12 à 20.  
  Pour que les 15ᵉ et 16ᵉ soient 8, il faut au moins **5 valeurs égales à 8** dans la classe 8–11 (elles occuperont les positions 12–16 et donc 15 et 16 seront 8).

### Une construction possible (valeurs explicites)
Choisissons (min, max) = **(3, 18)** (donc étendue = 15). On construit la série ainsi :

- **Classe 0–3** (5 élèves) → 5 × **3**  
- **Classe 4–7** (6 élèves) → 6 × **7**  
- **Classe 8–11** (9 élèves) → **5 × 8**, **1 × 9**, **1 × 10**, **2 × 11**  
  (ainsi on a au moins 5 valeurs égales à 8 → la 15ᵉ et la 16ᵉ seront 8)  
- **Classe 12–15** (6 élèves) → 6 × **15**  
- **Classe 16–20** (4 élèves) → 4 × **18**

Vérifions :

- Effectifs : 5 + 6 + 9 + 6 + 4 = **30** ✅  
- Somme des notes :
  - classe 0–3 : \(5\times 3 = 15\)  
  - classe 4–7 : \(6\times 7 = 42\)  
  - classe 8–11 : \(5\times 8 + 1\times 9 + 1\times 10 + 2\times 11 = 40 + 9 + 10 + 22 = 81\)  
  - classe 12–15 : \(6\times 15 = 90\)  
  - classe 16–20 : \(4\times 18 = 72\)  
  Total = \(15 + 42 + 81 + 90 + 72 = 300\). Moyenne = \(300/30 = 10\). ✅
- Étendue : max − min = 18 − 3 = **15**. ✅
- Médiane : positions 1–11 ≤ 7, positions 12–20 = valeurs de la classe 8–11. Dans la classe 8–11 on a **5 valeurs égales à 8** au début → positions 12,13,14,15,16 sont 8 → la moyenne des 15ᵉ et 16ᵉ = (8+8)/2 = **8**. ✅

### Une série complète (triée) possible
3,3,3,3,3, (5 valeurs dans 0–3)
7,7,7,7,7,7, (6 valeurs dans 4–7)
8,8,8,8,8,9,10,11,11, (9 valeurs dans 8–11 : 5×8, 9, 10, 2×11)
15,15,15,15,15,15, (6 valeurs dans 12–15)
18,18,18,18 (4 valeurs dans 16–20)
Cette série respecte **toutes** les contraintes demandées.
