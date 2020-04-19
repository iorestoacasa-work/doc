IoRestoACasa.work - Multiparty Meeting
======================================

Il software Multiparty Meeting è un software più moderno di Jitsi Meet,
ed è stato sviluppato nell'ambito del progetto EduMeet del GARR.

* Repository di sviluppo upstream: https://github.com/havfo/multiparty-meeting
* Repository nostra installazione docker ed esportazione metriche iorestoacasa.work: https://github.com/iorestoacasa-work/mm

Opzioni di configurazione più usate
-----------------------------------

Il branding dell'applicazione (nome/logo) si può fare impostando

.. todo: ci sono? 


Customizzazione per la musica
-----------------------------

Dario, maestro di pianoforte, aveva bisogno di rimuovere i fruscii per avere una migliore qualità audio

.. todo: da rivedere @tapion o Dario

aggiungendo:

`config.disableHPF=true&config.disableAGC=true&disableNS=true&config.disableAEC=true&config.disableAP=true&config.stereo=true`

nella barra degli indirizzi si eliminano i processi dell'audio, con @tapion li abbiamo eliminati anche dal server come default


Possibilità per ogni canale
--------------------------

c'è un limite di 500 consumer per ogni stanza su MM. Ogni flusso audio / video utilizza un consumer.
significa che in una stanza con lastN 10 possono entrare 25 persone massimo.

con lastN 1, possono entrare 250 persone.

pensiamo sia un limite di mediasoup (TODO .. todo: da trovare riferimento)


Integrazione ulteriori servizi
------------------------------

MM si può integrare con vari LMS (Learning Management System) tramite API LTI come descritto all'URL: 
https://github.com/havfo/multiparty-meeting/blob/master/LTI/LTI.md

È oltremodo facile farlo con Moodle per la presenza di un plugin come scritto in fondo alla pagina dell'URL precedente.





