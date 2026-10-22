```mermaid

erDiagram
    Personatge {
        string DNI PK
        string Nom NOT NULL
        string Cognom NOT NULL
        int Vida
        int Força
        int Agilitat
        int Carisma
    }
    Item {
        string Codi PK
        string Nom NOT NULL
        Boolean Equipable
        Boolean Comerciable NOT NULL 
        string Tipus NOT NULL
        int Pes NOT NULL
        int Qualitat NOT NULL
        int Medidas NOT NULL
    }
    Mascota {
        string  Num.Chip PK
        string Nom NOT NULL
        Boolean Motxilla 
    }
    Enemic {
        string Codi PK
        string Nom NOT NULL
        string Tipus NOT NULL
        int Nivell 
        int Vida
        int Força
        int Agilitat
        int Carisma
    }
    Habilitat {
        string Codi PK
        string Nom NOT NULL
        int Cost 
        int Dany
        float Cooldown
        string Tipus NOT NULL
    }

    Personatge }| -- o{ Item: "Equipa"
    Mascota }| -- o{ Item: "Carrega"
    Personatge || -- || Mascota: "Acompanya"
    Personatge }| -- |{ Enemic: "Enfrenta"
    Personatge }| -- o{ Habilitat: "Poseeix"
    Enemic }| -- |{ Habilitat: "Enfrenta"
    Habilitat }| -- |{ Habilitat: combina_amb
```
