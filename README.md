# Quadra - Soundscape Polar Controller

Quadra è un plugin che converte coordinate polari in coordinate cartesiane per il sistema d&b Soundscape.  
Permette di trasferire automazioni ambisonic dal plugin IEM Stereo Encoder al plugin d&b Soundscape,  
utilizzando messaggi MIDI CC a 14 bit.

## Funzionamento

1. Il plugin IEM Stereo Encoder genera automazioni ambisonic.
2. Quadra converte le coordinate polari in coordinate cartesiane.
3. Le coordinate X e Y vengono inviate come messaggi MIDI CC 14-bit.
4. Il plugin d&b Soundscape riceve i dati e controlla la posizione del suono.

## Routing MIDI

- X: CC 1-33
- Y: CC 2-34

Il MIDI output di Quadra deve essere inviato al plugin d&b Soundscape.

## Esempio

Di seguito un esempio del funzionamento di Quadra in Reaper.

![Quadra in azione](video.gif)

## Simulazione 3D

Questa immagine mostra la trasformazione delle coordinate nello spazio.

![Simulazione 3D](image.png)

## Installazione

1. Caricare Quadra come plugin MIDI in Reaper.
2. Collegare le automazioni dal plugin IEM Stereo Encoder.
3. Instradare l'output MIDI di Quadra verso il plugin d&b Soundscape.

## Licenza

Questo progetto è distribuito sotto licenza MIT.
