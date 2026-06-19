Procédure dot_product(v1, v2, m, ps)

Variables
    i : entier

Début
    ps ← 0

    Pour i ← 1 à m Faire
        ps ← ps + v1[i] * v2[i]
    FinPour
Fin

Algorithme Orthogonalite_Procedure

Variables
    n, m, i, j : entier
    v1, v2 : tableau[1..100] de réel
    ps : réel

Début

    Lire(n)     // nombre de couples de vecteurs

    Pour i ← 1 à n Faire

        Lire(m) // dimension des vecteurs

        Pour j ← 1 à m Faire
            Lire(v1[j])
        FinPour

        Pour j ← 1 à m Faire
            Lire(v2[j])
        FinPour

        Appeler dot_product(v1, v2, m, ps)

        Si ps = 0 Alors
            Ecrire("Les vecteurs sont orthogonaux")
        Sinon
            Ecrire("Les vecteurs ne sont pas orthogonaux")
        FinSi

    FinPour

Fin