IoRestoACasa.work - Jitsi Meet
==============================

Il software Jitsi Meet è un software libero rilasciato in licenza ...

* Repository di sviluppo upstream: https://github.com/jitsi 
* Repository nostra installazione docker ed esportazione metriche iorestoacasa.work: https://github.com/iorestoacasa-work/docker-jitsi-meet

Opzioni di configurazione più usate
-----------------------------------

Il branding dell'applicazione (nome/logo) si può fare impostando ...

Si sta cercando di alleggerire il carico sui client e se ne discute nelle 

* `issue #39 <https://github.com/iorestoacasa-work/iorestoacasa.work/issues/39>`_
* `issue #46 <https://github.com/iorestoacasa-work/iorestoacasa.work/issues/46>`_

Aggiornare la lingua all'ultima versione
----------------------------------------

Guida by Ermann del 22/04/2020

abbiamo testato il metodo funzionante per aggiornare la traduzione italiana con quella corretta rilasciata sul repo di jitsi, 
ecco la procedura:

.. sourcecode:: bash

  # docker exec -it docker-jitsi-meet_web_1 bash
  # apt-get update
  # apt-get install nano (io ho installato nano come editor)
  # nano /usr/share/jitsi-meet/lang/main-it.json
  # (da https://raw.githubusercontent.com/jitsi/jitsi-meet/master/lang/main-it.json ho fatto un semplice "copia e incolla" dal web al file)
  # exit (dall'immagine docker-jitsi-meet_web_1)
  
  # docker-compose stop
  # sudo rm -rf .jitsi-meet-cfg/
  # sudo rm -rf ~/.jitsi-meet-cfg/
  # docker ps -a
  # docker commit CONTAINER_ID jitsi/web
  # docker-compose up -d

Integrazione ulteriori servizi
------------------------------

È possibile integrare by design vari servizi:

* Etherpad: https://github.com/iorestoacasa-work/iorestoacasa.work/issues/21
* Streaming YouTube: https://github.com/iorestoacasa-work/iorestoacasa.work/issues/25
* Registrazione su Dropbox: https://github.com/iorestoacasa-work/iorestoacasa.work/issues/26

Affrontare le issues e scrivere qui brevi indicazioni di come si possono abilitare nei server di IoRestoACasa.work
