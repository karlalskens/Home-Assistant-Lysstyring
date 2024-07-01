# HAlysstyring
Dette er et system for å styre lyssoner i Home Assistant. Det kan både styres med bevegelsessensorer og brukerknapper, og lyset endrer seg etter om det er dagslys ute eller ikke.

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fkarlalskens%2FHome-Assistant-Lysstyring%2Fblob%2Fmain%2Fblueprints%2Fautomation%2Fkarlalskens_Lysstyring%2FAutomatisk_Lysstyring.yaml)

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
