
# 📘 Instructions Installation – TP Python Data Science (Mode OFFLINE)

⚠️ **Important**  
L’environnement virtuel nommé **`virtuel`** a déjà été créé et configuré par l’enseignant.  
👉 Vous **n’avez PAS** besoin d’installer Python, ni de créer un environnement virtuel.

---

## 1️⃣ Ouvrir le projet dans VS Code

1. Copier le dossier du projet (clé USB / partage)
2. Ouvrir **VS Code**
3. Cliquer sur **File → Open Folder**
4. Sélectionner le dossier du projet

---

## 2️⃣ Installer les extensions VS Code (OFFLINE)

Si les extensions ne sont pas encore installées :

1. Ouvrir VS Code
2. Aller dans **Extensions**
3. Cliquer sur **⋯ → Install from VSIX**
4. Installer les fichiers :
   - `python.vsix`
   - `jupyter.vsix`

---

## 3️⃣ Adapter le chemin Python (IMPORTANT)

Ouvrir le fichier suivant :
```
virtuel/pyvenv.cfg
```

Modifier la ligne `home` selon votre PC :

```txt
home = C:\Users\VOTRE_NOM\AppData\Local\Programs\Python\Python310
include-system-site-packages = false
version = 3.10.11
```

📌 Remplacer **VOTRE_NOM** par votre nom d’utilisateur Windows.

---

## 4️⃣ Activer l’environnement virtuel

Dans VS Code :
1. Ouvrir le **Terminal**
2. Exécuter :

```bash
virtuel\Scripts\activate
```

Vérification :
```bash
python --version
```

Résultat attendu :
```text
Python 3.10.11
```

---

## 5️⃣ Choisir le Kernel Jupyter

1. Ouvrir le fichier `main.ipynb`
2. En haut à droite → **Select Kernel**
3. Choisir :
```
Python 3.10 (virtuel)
```

---

## 6️⃣ Tester l’environnement

### Test Python
```python
print("TP Python prêt !")
```

### Test NumPy
```python
import numpy as np
np.array([1, 2, 3]) * 2
```

### Test Pandas
```python
import pandas as pd

df = pd.DataFrame({
    "nom": ["Aina", "Rado", "Miora"],
    "age": [20, 22, 19]
})

df
```

---

## ✅ Fin
Si tout fonctionne :
✔ environnement prêt  
✔ bibliothèques fonctionnelles  
✔ prêt pour les TP Data Science

---

.*
