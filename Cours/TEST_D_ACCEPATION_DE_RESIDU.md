# I. TEST POUR ACCEPTE LE RESIDU
### **1️⃣ Ljung–Box (Q test)**
👉 Test d’autocorrélation des résidus\
🎯 **Objectif**: Vérifier si les résidus sont indépendants (bruit blanc).\
**🔹 Hypothèses**\
$H_0$ (hypothèse nulle) :
👉 Les résidus ne sont PAS autocorrélés (bruit blanc)\
$H_1$:
👉 Les résidus sont autocorrélés\
**🔹 Interprétation**\
- p-value > 0.05 ✅\
→ résidus indépendants → modèle acceptable
- p-value ≤ 0.05 ❌\
→ autocorrélation restante → modèle mal spécifié\
**🔧 Que faire si Ljung-Box échoue ?**
1. Augmenter p ou q
2. Ajouter un terme saisonnier (P ou Q)
3. Augmenter d ou D
4. Vérifier la saisonnalité oubliée\
📌 En clair :
Le modèle n’a pas capturé toute la structure temporelle

### **2️⃣ Jarque–Bera (JB)**
👉 Test de *normalité des résidus*\
**🎯 Objectif**: Vérifier si les résidus suivent une loi normale
**🔹 Hypothèses**\
$H_0$  : résidus normaux\
$H_1$ : résidus non normaux\
**🔹 Interprétation**
- p-value > 0.05 ✅\
→ normalité acceptée
- p-value ≤ 0.05 ❌\
→ résidus non normaux\
**🔧 Que faire si JB échoue ?**
⚠️ Ce n’est PAS critique pour la prévision\
Mais tu peux :
1. Appliquer une transformation (log, Box-Cox)
2. Supprimer les outliers
3. Utiliser des intervalles robustes
4. Passer à GARCH si variance changeante

**📌 Important**:SARIMA peut très bien prédire même avec des résidus non normaux

### **3️⃣ Heteroskedasticity (H)**
👉 Test de variance non constante\
🎯 **Objectif**: *Vérifier si la variance des résidus est constante*
**🔹 Hypothèses**\
$H_0$ : variance constante (homoskédasticité)\
$H_1$ : variance variable (hétéroskédasticité)\
**🔹 Interprétation**
- p-value > 0.05 ✅\
→ variance stable
- p-value ≤ 0.05 ❌\
→ variance instable

**🔧 Que faire si H échoue ?**
**Transformation log / Box-Cox**
- Modèle SARIMA + GARCH
- Modèle ETS ou Prophet
- Différenciation supplémentaire

# II. **Rappel : que signifie la colonne P>|z| ?**
- P-value = probabilité que le coefficient soit nul
- Règle classique :
    - p < 0.05 → coefficient significatif
    - p ≥ 0.05 → coefficient non significatif

### **Analyse coefficient par coefficient**
- Coefficient ar.L1 pour le paramétre **AR(p)** 
    - p < 0.05 → coefficient significatif donc le parametre p est bien
    - p ≥ 0.05 → coefficient non significatif donc le parametre p n'est pas bien

- Coefficient ma.L1 pour le paramétre **MA(q)**
    - p < 0.05 → coefficient significatif donc le parametre q est bien
    - p ≥ 0.05 → coefficient non significatif donc le parametre q n'est pas bien
- Coefficient ma.S.L12 pour le parametre **AR(P) saisonnier**
    - p < 0.05 → coefficient significatif donc le parametre P est bien
    - p ≥ 0.05 → coefficient non significatif donc le parametre P n'est pas bien
- Coefficient sigma2 pour le parametre **MA(Q) saisonnier**
    - p < 0.05 → coefficient significatif donc le parametre Q est bien
    - p ≥ 0.05 → coefficient non significatif donc le parametre Q n'est pas bien

# III. **AIC, BIC, HQIC**
### **1️⃣ AIC – Akaike Information Criterion**
**🔹 Signification**
- AIC mesure le compromis entre :
    - la qualité d’ajustement du modèle
    - la complexité (nombre de paramètres):
    $AIC = -2\log(L) +2k$
        - $L$ : Vraisemblance (log Likelihood)
        - $k$ : nombre de paramères\
**🔹 Comment l’interpréter ?**
- Plus AIC est petit → meilleur modèle
- AIC n’a PAS d’échelle absolue
    **Rémarque** : Un AIC seul ne veut rien dire
### **2️⃣ BIC – Bayesian Information Criterion**
**🔹 Signification**
- BIC pénalise fortement la complexité
    $BIC = -2\log(L) +k\log(n)$
    - $n$: nombre d'observation\
**🔹 Comment l’interpréter ?**
- Plus petit = meilleur
- Favorise les modèles simples
- Très utilisé en économétrie
### **3️⃣ HQIC – Hannan–Quinn Information Criterion**
**🔹 Signification**
- Compromis entre AIC et BIC
- Pénalisation modérée
    $HQIC=-2\log(L)+2k\log(\log(n))$\
**🔹 Comment l’interpréter ?**
- plus petit = meilleur