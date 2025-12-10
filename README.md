# My first GitHub Project 
# Chef de projet: Bouchentouf marwa, Master1 Biochimie , (6/12/2025)
# Membres  de l'équipe:
# leshaf wafaa
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
