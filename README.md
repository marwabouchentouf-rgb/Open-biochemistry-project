# My first GitHub Project 
# Chef de projet: Bouchentouf marwa, Master1 Biochimie , (6/12/2025)
# Membres  de l'équipe:
# leshaf wafa
# Bouayed meryem
# belarbi dounia
# belarbi hanane
# bennaceur fatima zohra douaa
import pandas as pd

# 1) Données: Séquences ADN, Longueur, Pourcentage de GC
data = {
        "Séquence": ["ATGCGTACGTA", "GCTAGCTAGGCC", "ATGCGCGTAAGT","TACGATCGTA", "ATGAAAGGCTT", "CGTACGTAGC", "TTAACCGGAT"],
        "Longueur": [12, 12, 12, 10, 11, 10, 10],
        "Pourcentage GC": [50, 66.67, 58.33, 40, 45.45, 60, 50]
}

# 1) Création d'un DataFrame (tableau pandas)
df = pd.DataFrame(data)
print("**** Creation et affichage *****")
print(df)

# 2) Sélection et affichage uniquement la colonne Longueur
print("\n=== Colonne Longueur ===")
print(df["Longueur"])

# 3) filtrage longueur > 10
print("\n=== séquences longueur > 10 ===")
print(df[df["longueur"] > 10], "\n\n")

# 4) Moyenne %GC (3 décimales)
moyenne_gc = df["pourcentage GC"].mean()
print(f"\nPourcentage moyen GC : {moyenne_gc:.3f}%", "\n\n")

# 5) catégorie GC
def catégorie_gc(gc):
    if gc > 55:
       return "Riche".
    elif gc >= 45:
        return "Moyen"
    else:
        return "Faible"
        
df["catégorie GC"] = df["pourcentage GC"].apply(catégorie_gc)
         
# 6) Nombre de G
df["Nb_G"] = df["Séquence"].apply(lambda seq:  seq.count("G"))
