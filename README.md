Query in MongoCompass

1. Trova tutte le risorse con il dato isActive corrispondente a true.

    Query utilizzata: {isActive : {$eq: true}}
    Risultati: 51

2. Trova tutte le risorse con il dato age maggiore di 26.

    Query utilizzata: {age : {$gt: 26}} ----- {age : {$gte: 26}} (gte= maggiore uguale)
    Risultati: 54 ---- 64

3. Trova tutte le risorse con il dato age maggiore di 26 e minore o uguale a 30.
    
    Query utilizzata: {age: {$gt:26, $lte: 30}}
    Risultati: 19

4. Trova tutte le risorse con il dato eyes che sia brown o blue.
    
    Query utilizzata: {$or: [{eyeColor: "brown"}, {eyeColor: "blue"}]}
    Risultati: 66

5. Trova tutte le risorse che non presentano il dato eyes uguale a green.
    
    Query utilizzata: {eyeColor: {$ne: "green"}}
    Risultati: 66

6. Trova tutte le risorse che non presentano il dato eyes uguale a green e neanche blue.
    
    Query utilizzata: {$nor: [{eyeColor: "green"}, {eyeColor: "blue"}]}
    Risultati: 35

7. Trova tutte le risorse con il dato company uguale a "FITCORE" e ritorna solo l'email.
    
    Query utilizzata: {company: "FITCORE", email: {$exists: true}}
    Risultati: 1

    