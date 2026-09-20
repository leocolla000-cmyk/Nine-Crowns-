# Nine Crowns v1.2.0 — Minecraft Java 26.1 / Fabric

Questa versione corregge il problema del JAR vuoto. La build ora **fallisce apposta** se il JAR non contiene davvero la mod.

## Corona dell'Imperatore
- Protection VIII
- Unbreaking III
- Mending
- Speed II mentre indossata
- Strength II mentre indossata
- Fire Resistance I mentre indossata

## Test rapido dopo l'installazione
1. Apri Mod Menu: deve comparire **Nine Crowns**.
2. Entra in un mondo/server Fabric 26.1.
3. Scrivi `/ninecrowns`: deve rispondere con `(1/9)` al primo ingresso.
4. Muori in un posto sicuro: deve apparire `Testa di <nome>`.

## Build GitHub
Il workflow `.github/workflows/build.yml` usa Java 25 + Gradle 9.5.1 e controlla che il JAR contenga:
- `fabric.mod.json`
- `NineCrowns.class`
- `ModItems.class`
- almeno 10 classi compilate

Se GitHub mostra il tick verde, l'artifact da scaricare si chiama:
`NineCrowns-26.1-v1.2.0-VERIFIED`

e contiene:
`ninecrowns-26.1-1.2.0.jar`

**Importante:** su GitHub i file devono mantenere le cartelle. Nella root devi vedere `src`, `.github`, `build.gradle`, `settings.gradle` e `gradle.properties`. Non devono comparire `NineCrowns.java`, `ModItems.java`, ecc. direttamente nella root.
