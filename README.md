# Polygon-Area-calculator
📐 Polygon Area Calculator | Projet Python orienté objet (POO) réalisé pour la certification freeCodeCamp.
# Calculateur d'Aire de Polygones — Polygon Area Calculator

[Français](#français) | [English](#english)

---

## <a name="français"></a> 🇫🇷 Version Française

# Calculateur d'Aire de Polygones (Polygon Area Calculator)

Ce projet contient deux classes Python, `Rectangle` et `Square` (Carré), permettant de créer des formes géométriques, de modifier leurs dimensions, de calculer leurs propriétés (aire, périmètre, diagonale), et même de les dessiner sous forme de texte.

Ce projet fait partie des défis de certification **Scientific Computing with Python** de freeCodeCamp.

---

## 🚀 Fonctionnalités

### 📐 Classe `Rectangle`
Permet de créer un rectangle en fournissant sa largeur (`width`) et sa hauteur (`height`).
* **Calculs :** Aire, périmètre et diagonale.
* **Dessin :** Génère une représentation visuelle du rectangle avec des étoiles `*` (jusqu'à une taille maximale de 50).
* **Imbrication :** Calcule combien de fois un autre rectangle ou carré peut rentrer à l'intérieur (sans rotation).

### 🟩 Classe `Square` (Sous-classe de `Rectangle`)
Permet de créer un carré en fournissant uniquement la longueur d'un côté (`side`).
* **Héritage :** Profite automatiquement de toutes les fonctionnalités de calcul et de dessin de la classe `Rectangle`.
* **Cohérence :** Si vous modifiez la largeur ou la hauteur du carré, l'autre dimension s'ajuste automatiquement pour que la forme reste un carré parfait.

---

## 🛠️ Utilisation et Exemples

Voici comment utiliser les classes dans un script Python :

```python
from shape_calculator import Rectangle, Square

# --- EXEMPLE 1 : LE RECTANGLE ---
rect = Rectangle(10, 5)
print(rect) # Affiche : Rectangle(width=10, height=5)
print("Aire :", rect.get_area()) # Affiche : 50
print("Périmètre :", rect.get_perimeter()) # Affiche : 30

# Modifier les dimensions
rect.set_height(3)
print(rect.get_picture())
# Affiche :
# **********
# **********
# **********

# --- EXEMPLE 2 : LE CARRÉ ---
sq = Square(5)
print(sq) # Affiche : Square(side=5)
print("Aire du carré :", sq.get_area()) # Affiche : 25

# Modifier un côté change automatiquement l'autre
sq.set_width(4)
print(sq) # Affiche : Square(side=4)

# --- EXEMPLE 3 : IMBRICATION ---
rect_grand = Rectangle(15, 10)
carre_petit = Square(5)
# Combien de carrés de 5x5 rentrent dans un rectangle de 15x10 ?
print(rect_grand.get_amount_inside(carre_petit)) # Affiche : 6
```

---

## 🧪 Contraintes techniques respectées

* **Programmation Orientée Objet :** La classe `Square` est un enfant de `Rectangle` (héritage). Un objet carré est reconnu par Python comme étant à la fois une instance de `Square` et de `Rectangle`.
* **Affichage textuel personnalisé :** Utilisation des méthodes magiques `__str__` pour un affichage propre dans la console.


---

## <a name="english"></a> 🇬🇧 English Version

# Polygon Area Calculator

This project contains two Python classes, `Rectangle` and `Square`, allowing you to create geometric shapes, modify their dimensions, calculate their properties (area, perimeter, diagonal), and even draw them using text representation.

This project is part of the **Scientific Computing with Python** certification challenges on freeCodeCamp.

---

## 🚀 Features

### 📐 `Rectangle` Class
Allows you to create a rectangle by providing its `width` and `height`.
* **Calculations:** Area, perimeter, and diagonal.
* **Drawing:** Generates a visual text representation of the rectangle using asterisks `*` (up to a maximum size of 50).
* **Nesting:** Calculates how many times another rectangle or square can fit inside the shape (with no rotations).

### 🟩 `Square` Class (Subclass of `Rectangle`)
Allows you to create a square by providing only a single `side` length.
* **Inheritance:** Automatically benefits from all calculation and drawing features of the `Rectangle` class.
* **Consistency:** If you modify the square's width or height, the other dimension automatically adjusts so that the shape remains a perfect square.

---

## 🛠️ Usage and Examples

Here is how to use the classes in a Python script:

```python
from shape_calculator import Rectangle, Square

# --- EXAMPLE 1: THE RECTANGLE ---
rect = Rectangle(10, 5)
print(rect) # Outputs: Rectangle(width=10, height=5)
print("Area:", rect.get_area()) # Outputs: 50
print("Perimeter:", rect.get_perimeter()) # Outputs: 30

# Modify dimensions
rect.set_height(3)
print(rect.get_picture())
# Outputs:
# **********
# **********
# **********

# --- EXAMPLE 2: THE SQUARE ---
sq = Square(5)
print(sq) # Outputs: Square(side=5)
print("Square Area:", sq.get_area()) # Outputs: 25

# Modifying one side automatically changes the other
sq.set_width(4)
print(sq) # Outputs: Square(side=4)

# --- EXAMPLE 3: NESTING ---
large_rect = Rectangle(15, 10)
small_square = Square(5)
# How many 5x5 squares fit inside a 15x10 rectangle?
print(large_rect.get_amount_inside(small_square)) # Outputs: 6
```

---

## 🧪 Technical Constraints Met

* **Object-Oriented Programming:** The `Square` class is a child of `Rectangle` (inheritance). A square object is automatically recognized by Python as an instance of both `Square` and `Rectangle`.
* **Custom String Representation:** Built-in `__str__` magic methods are implemented to ensure clean formatting when printing objects to the console.

