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
