Algorithme SommeElementsDistincts

Variables
    T1, T2 : tableaux de réels
    n1, n2 : entiers
    i, j : entiers
    trouve : booléen
    somme : réel

Début

    Lire(n1)
    Pour i ← 1 à n1 Faire
        Lire(T1[i])
    FinPour

    Lire(n2)
    Pour i ← 1 à n2 Faire
        Lire(T2[i])
    FinPour

    somme ← 0

    // Éléments de T1 absents de T2
    Pour i ← 1 à n1 Faire
        trouve ← Faux

        Pour j ← 1 à n2 Faire
            Si T1[i] = T2[j] Alors
                trouve ← Vrai
            FinSi
        FinPour

        Si trouve = Faux Alors
            somme ← somme + T1[i]
        FinSi

    FinPour

    // Éléments de T2 absents de T1
    Pour i ← 1 à n2 Faire
        trouve ← Faux

        Pour j ← 1 à n1 Faire
            Si T2[i] = T1[j] Alors
                trouve ← Vrai
            FinSi
        FinPour

        Si trouve = Faux Alors
            somme ← somme + T2[i]
        FinSi

    FinPour

    Ecrire("Somme des éléments distincts = ", somme)

Fin