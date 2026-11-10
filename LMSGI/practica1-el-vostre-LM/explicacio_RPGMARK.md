# RPGMARK

## Que es RPGMARK?
- RPGMARK es un llenguatge de marques semantic.
- La seva utilitat es guardar configuracions de builds a diferents videojocs.
- El llenguatge es semantic ja que n'utilitzem etiquetas com `<weapons>` o `<armor>` per definir les dades a les builds.

## Reglas d'RPGMARK
- Cada build comença amb l'etiqueta `<build:>` i es tanca amb l'etiqueta `<dluib>`.
- Cada seccio de la build es tanca amb l'invers del nom de la seccio, per exemple:
```
  <build: ER>
    <hand>
      <left: >
      <right: >
    <dnah>
  <dliub>
```
  - Si la seccio en té un guionet, s'inverteix les paraules separades pel guionet, per exemple:
    
```
  <build: ER>
    <player-stats>
      <int: str = 10>
    <stats-player>
  <dliub>
```

- Les dades en si s'escriuen `<camp: valor>`, i les estaditiques s'escriuen com `<int: nom = valor>`.

> [!NOTE]
> Aquest llenguatge seria util per persones que volen fer build o configuracions de builds especifiques a diferents jocs, una aplicacio pot lleguir el fitxer i interpretar-ho directament amb el seu diseny, es pot filtrar per armadura, armes i estadistiques.

## Perque es RPGMARK un llenguatge de marques?
- Es pot obrir i escriure amb qualsevol editor aixi doncs solament utitlitza text pla.
- Utitlitza metadades, es a dir etiquites i atributs que descriuen cada dada com hem vist anteriorment.
- Un programa pot llegir cada dada per la seva etiqueta.
- La mateixa build es pot visualitzar de diferents maneres ja que l'informacio i l'estructura sempre sera la mateixa.

## Exemple final

```

<build: SEKIRO>

<player>
  <name: >
  <weapon: >
  <secondary: >
<reyalp>

<prosthetic>
  <tool: >
  <tool: >
  <tool: >
<citehtsorp>

<skills>
  <combat-art: >
  <passive: >
  <passive: >
<slliks>

<player-stats>
  <int: vitality = 20>
  <int: attack-power = 14>
  <int: posture = 100>
<stats-player>

<dliub>

```
  
