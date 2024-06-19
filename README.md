# HAlysstyring
Dette er et system for å styre lyssoner i Home Assistant. Det kan både styres med bevegelsessensorer og brukerknapper, og lyset endrer seg etter om det er dagslys ute eller ikke.

1. Opprette Helper-verdier for hvert område
2. Opprette scener for hvert område
3. Blueprint-automasjon for tidsstyring
4. Blueprint-skript for aktivering av scener
5. Blueprint for skifte av scener ved soloppgang/-nedgang
6. Blueprint for oppdatering av treige sensorer

## Helper-verdier for hvert område
Opprett hjelpeverdier for hvert område. Dette er variablene som lagrer om et område er aktkivt eller passivt. Dette er også verdier som kan være tilgjengelig for brukerene.

> [!TIP]
> Hvis noen er tilstede i et område skal det være "aktivt". Hvis det ikke er noen tilstede er området "passivt".

```
input_boolean:
  # Repeter koden under og bytt ut Område1 med navnet på området, f.eks Stua.
  Tilstede_Område1:
    name: Lys på i område 1
    initial: off
  deaktiver_lysstyring_Område1:
    name: Bevegelse i område 1
    initial: off
```
## Scener for hvert område
Opprett scener for hvert område. Må følge navnekonvensjon for å kunne brukes av skriptet under.

## Blueprint-automasjon for tidsstyring
Denne automasjonen aktiverer og deaktiverer booleanverdien for området. Den trigges av binære sensorer som bevegelsessensorer, og deaktiverer etter angitt tid uten nye impulser.

## Blueprint-skript for aktivering av scener


## Blueprint for skifte av scener ved soloppgang/-nedgang


## Blueprint for oppdatering av treige sensorer
Enkelte typer bevegelsessensorer tar veldig lang tid fra status endres fra Opptatt til Klar. For å kunne bruke den i bevegelsesautomasjoner kan den oversettes til en binærsensor som skifter verdi oftere. Det vil si, den endrer status samtidig med sensoren, og så lenge sensoren fremdeles er Opptatt veksler en gang per minutt.