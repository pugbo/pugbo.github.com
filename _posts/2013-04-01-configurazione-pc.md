---
layout: post
title: Configurare il vostro sistema per EvenThor
tagline: virtualbox, vagrant e tutto il resto
tags: configurazione vagrant virtualbox
---
{% include JB/setup %}
Ora che facciamo sul serio non ci resta che configurare le nostre macchine per
**lavorare su EvenThor**. Dopo avere installato gli strumenti necessari
i passi per avere una copia di lavoro **immediatamente funzionante** sono davvero
pochi, anzi uno! Basta infatti lanciare ```vagrant up``` ed al resto pensa tutto lui!

## Strumenti necessari
* git
* ruby
* virtualbox 4.x
* NFS
* vagrant 1.1.x 

## Installazione
Qui di seguito sono descritti i passi da effettuare, differenziati per sistema
operativo.
### Ubuntu e Mac
1. Installate ruby, se non lo avete già fatto
2. Installare NFS, su ubuntu il pacchetto si chiama ```nfs-kernel-server```

### Ubuntu: repository Oracle (opzionale)
Se volete installare l'ultima versione di VirtualBox su ubuntu potete utilizzare i repository di Oracle, mediante tre semplici passi:

1. ```echo deb http://download.virtualbox.org/virtualbox/debian `lsb_release -sc` contrib | sudo tee /etc/apt/sources.list.d/virtualbox.list```
2. ```wget -q http://download.virtualbox.org/virtualbox/debian/oracle_vbox.asc -O- | sudo apt-key add -```
3. ```sudo apt-get update```

In questo caso il pacchetto da installare sarà virtualbox-4.2, se preferite
invece il repository standard dovrete installare il pacchetto virtualbox.

### Ubuntu, Windows e Mac
1. Installate git, se usate Windows la versione consigliata è [msysGit](http://msysgit.github.com/)
3. Installate virtualbox scaricandolo dal [sito ufficiale](https://www.virtualbox.org/) o tramite repository
4. Installate il pacchetto Vagrant rigorosamente scaricato dal [sito ufficiale](http://downloads.vagrantup.com/)

## Fork del repository
Il progetto sarà completamente gestito mediante **pull request**, per far si che
ogni riga di codice sia visionata da un secondo sviluppatore prima che venga
inserita all'interno del progetto principale.

Ogni sviluppatore dovrà creare un proprio fork, GitHub ha pubblicato un tutorial
molto chiaro (in inglese) su come creare un fork e soprattutto come **mantenerlo allineato**
al ramo di sviluppo principale [https://help.github.com/articles/fork-a-repo](https://help.github.com/articles/fork-a-repo).
