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
  Tilstede_område1:
    name: Lys på i område 1
    initial: off
  deaktiver:
    name: Bevegelse i område 1
    initial: off
    
    # Repeter for hvert område

```


## Scener for hvert område


## Blueprint-automasjon for tidsstyring


## Blueprint-skript for aktivering av scener


## Blueprint for skifte av scener ved soloppgang/-nedgang


## Blueprint for oppdatering av treige sensorer
Enkelte typer bevegelsessensorer tar veldig lang tid fra status endres fra Opptatt til Klar. For å kunne bruke den i bevegelsesautomasjoner kan den oversettes til en binærsensor som skifter verdi oftere. Det vil si, den endrer status samtidig med sensoren, og resettes en gang per minutt.