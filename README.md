# Canal de actualizaciones de VoiceFlow

Aquí vive el *appcast* que consulta [Sparkle](https://sparkle-project.org) y los paquetes
de cada versión. **No hay código fuente en este repositorio**, y es público porque la app
tiene que poder descargar de aquí sin credenciales.

Lo genera `Tools/publicar.sh` del proyecto de VoiceFlow. Cada entrada del appcast va
firmada con EdDSA y la app rechaza cualquier descarga cuya firma no case con la clave
pública que lleva embebida: quien controle este repositorio o la red no puede colar una
versión adulterada.

Los `.zip` de versiones anteriores **no se borran**: el appcast los sigue listando y
quien vaya con retraso actualiza a través de ellos.
