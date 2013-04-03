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
### Ubuntu
1. Installate ruby
2. Installare il pacchetto ```nfs-kernel-server```
3. Installate git
4. Installate virtualbox scaricandolo dal [sito ufficiale](https://www.virtualbox.org/) o tramite repository
5. Installate il pacchetto .deb Vagrant (occhio all'architettura!) rigorosamente scaricato dal [sito ufficiale](http://downloads.vagrantup.com/)
6. (Opzionale) installate gitg e/o gitk per la visualizzazione grafica del repository

#### Repository Oracle (opzionale)
Se volete installare l'ultima versione di VirtualBox su ubuntu potete utilizzare i repository di Oracle, mediante tre semplici passi:

1. ```echo deb http://download.virtualbox.org/virtualbox/debian `lsb_release -sc` contrib | sudo tee /etc/apt/sources.list.d/virtualbox.list```
2. ```wget -q http://download.virtualbox.org/virtualbox/debian/oracle_vbox.asc -O- | sudo apt-key add -```
3. ```sudo apt-get update```

In questo caso il pacchetto da installare sarà virtualbox-4.2, se preferite
invece il repository standard dovrete installare il pacchetto virtualbox.

### Mac
1. Installate virtualbox scaricandolo dal [sito ufficiale](https://www.virtualbox.org/)
2. Installate il pacchetto .dmg di Vagrant rigorosamente scaricato dal [sito ufficiale](http://downloads.vagrantup.com/)
3. (Opzionale) Aggiornate git con homebrew ```brew install git git-flow``` 
3. (Opzionale) Installate [Atlassian SourceTree](http://www.sourcetreeapp.com/) per la visualizzazione grafica del repository

### Windows
1. Installate virtualbox scaricandolo dal [sito ufficiale](https://www.virtualbox.org/)
2. Installate il pacchetto .msi di Vagrant rigorosamente scaricato dal [sito ufficiale](http://downloads.vagrantup.com/)
3. Installate [Git for Windows](http://msysgit.github.com/)
3. (Opzionale) Installate [Atlassian SourceTree](http://www.sourcetreeapp.com/) per la visualizzazione grafica del repository

## Avviare la macchina virtuale
Per avviare la macchina virtuale è sufficiente digitare con una console dentro la directory vagrant

```vagrant up```

### Importante!
Testate il funzionamento della macchina virtuale prima della serata in modo
da evitare a priori inconvenienti tecnici.

## Fork del repository
Il progetto sarà completamente gestito mediante **pull request**, per far si che
ogni riga di codice sia visionata da un secondo sviluppatore prima che venga
inserita all'interno del progetto principale.

Ogni sviluppatore dovrà creare un proprio fork, GitHub ha pubblicato un tutorial
molto chiaro (in inglese) su come creare un fork e soprattutto come **mantenerlo allineato**
al ramo di sviluppo principale [https://help.github.com/articles/fork-a-repo](https://help.github.com/articles/fork-a-repo).
