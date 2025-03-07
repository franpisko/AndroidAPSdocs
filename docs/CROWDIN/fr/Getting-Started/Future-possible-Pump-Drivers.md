# Pilotes de pompe futurs (possibles)

Voici une liste de certaines pompes et leur statut de prise en charge dans l'un des systèmes en boucle, puis leur statut dans AAPS. En fin de compte, il y a quelques informations de ce qui est nécessaire pour qu'une pompe soit "bouclable".

## Pompes qui sont Bouclable

### Omnipod DASH ([Page d'accueil](https://www.myomnipod.com/DASH))

**Etat de la boucle :** Actuellement non prise en charge par aucun système de boucle. La pompe est compatible de la Boucle, mais le protocole inconnu à l'heure actuelle. La vente de la pompe a officiellement commencé en janvier 2019.

**Configuration matérielle requise pour AAPS :** Probablement aucune. Elle dispose du Bluetooth.

**Comments:** Group of developers is looking into protocol (by reverse engineering original app) and into solution for AAPS, now that pump has become available all over world. There are no estimations yet, when this will be available, or even when first testing will begin. If you are interested in progress, or are willing to help, group can be reachable on WeAreNotWaiting discord. Mention your interest in androidaps group and someone will give you more info.

* * *

### Pompe Ypsomed ([Page d'accueil](https://www.ypsomed.com/en/diabetes-care-mylife.html))

**Etat de la boucle :** Version 1-1.5 (2Q/2018) ne sont pas candidates à la boucle. While they do have BT communication, communication is very limited and uni directional: Pump->App. By end of 2021, it is planned that company will release, new version nicknamed DOSE (1.6), which will allow setting bolus and TBR from their App. They plan to implement their own Loop in 2022, with their own application. More info see this [page](https://www.mylife-diabetescare.com/en/loop-program.html)

**Hardware requirement for AAPS:** None. Elle dispose du Bluetooth.

**Comments:** There are currently 2 groups working on driver, so after new version is released, we can expect to have AAPS support soon thereafter. One group is being supported by YpsoMed and helping with Medical trials that are happening in Australia, 2nd is working independently by reverse engineering original app.

* * *

### Kaleido ([Page d'accueil](https://www.hellokaleido.com/))

**Etat de la boucle :** Actuellement non prise en charge par aucun système de boucle. Pump is a Loop candidate, but since protocol is unknown at the time, I am not seeing this pump supported very soon.

**Configuration matérielle requise pour AAPS :** Probablement aucune. Elle dispose du Bluetooth.

* * *

### Medtrum A6/P6/C6 ([Page d'accueil](https://www.medtrum.com/P6.html))

**Loop status:** Is a Loop candidate. Company has its own limited half-Loop system running (A6). Controlable via iPhone App. No Android app available at the moment.

**Configuration matérielle requise pour AAPS :** Probablement aucune. It seems to be BT enabled.

* * *

### EOFLOW ([Page d'accueil](http://www.eoflow.com/eng/main/main.html))

**Loop status:** Is a Loop candidate. The remote control they use is actually modified Android device. (Pump is currently available only in Korea).

**Configuration matérielle requise pour AAPS :** Probablement aucune. It seems to be BT enabled.

* * *

### Accu-Chek Solo ([Page d'accueil](https://www.roche.com/media/releases/med-cor-2018-07-23.htm))

**Loop status:** Is a Loop candidate. Pump will start selling at end of 2018 in selected countries in EU. Its rummored to have Android app on special controler device for control.

**Configuration matérielle requise pour AAPS :** Probablement aucune. It seems to be BT enabled.

### Medtronic Bluetooth

**Comments:** This is pump that will come out in next few years and is planned to be supported in Tidepool Loop software ([see this article](https://www.tidepool.org/blog/tidepool-loop-medtronic-collaboration).

### Pompe Insuline Willcare ([Page d'accueil](http://en.shinmyungmedi.com))

**Loop status:** At the moment its not Loop candidate, but we were contacted by their staff and they interested in extending their pump to be loopable (at the moment I think its missing only get/set profile commands).

**Hardware requirement for AAPS:** None. It seems to be BT enabled.

**Comments:** Since company is interested in integration with AAPS, they might do implementation themselves.

* * *

## Pompes plus vendues (les entreprises ne fonctionnent plus)

### Pompe Cellnovo ([voir businesswire.com](https://www.businesswire.com/news/home/20190328005829/en/Cellnovo-Stops-Manufacturing-and-Commercial-Operations))

**Etat de la boucle :** Actuellement non prise en charge par aucun système de boucle. Pump is a Loop candidate, but since protocol is unknown at the time, I am not seeing this pump supported very soon.

**Configuration matérielle requise pour AAPS :** Probablement aucune. Elle dispose du Bluetooth.

**Note about product:** It seems that company decided to exit the Pump Business. You can see more in this [article](https://diabetogenic.wordpress.com/2019/04/01/and-then-cellnovo-disappeared/?fbclid=IwAR12Ow6gVbEOuD1zw7aNjBwqj5_aPkPipteHY1VHBvT3mchlH2y7Us6ZeAU)

## Pompes qui ne sont pas bouclable

### Tandem : (toutes) ([Page d'accueil](https://www.tandemdiabetes.com/))

**Etat de la boucle :** Non bouclable.

While ago they had firmware called T:AP (mentioned in this [article](https://www.liebertpub.com/doi/full/10.1089/dia.2018.0278?url_ver=Z39.88-2003&rfr_id=ori%3Arid%3Acrossref.org&rfr_dat=cr_pub%3Dpubmed&), which could be used in loop (its no longer available, since pump was upgraded to x2), but that was not intended for commercial use, just for experimental use only (research projects). I talked with one of directors of company and he assured my that Tandem pump will never be open, but they have created their own closed loop system, which they are calling Control-IQ (I think it is already available in USA, and should be available in 2020 in Eu).

* * *

### Animas Vibe

**Etat de la boucle :** Non bouclable. No remote control possibility. **Note:** Pump is not being sold anymore. Company stopped working in Pump bussiness (J&J).

* * *

### Animas Ping

**Etat de la boucle :** Non bouclable. It has bolus possibility, but no TBR one. **Note** Stopped being sold when Vibe came out.

## Exigences pour que les pompes soient bouclables

**Prerequisite**

- La pompe doit prendre en charge un contrôle à distance (Bluetooth, fréquence radio, etc.).
- Le protocole est piraté/documenté/etc.

**Minimal requirement**

- Définir le Débit de Basal Temporaire
- Obtenir l'état de la pompe
- Annuler le Débit de Basal Temporaire

**For oref1(SMB) or Bolusing:**

- Définir le Bolus

**Good to have**

- Annuler le Bolus en cours
- Obtenir le profil de basal (presque requis)
- Définir le profil de basal (souhaitable)
- Lire l'historique 

**Other (not required but good to have)**

- Définir un bolus étendu
- Annuler Bolus étendu
- Lire l'historique
- Lire le TDI

* * *

### Prise en charge d'autres pompes

If you have any other pumps you would like to see status on, please contact us on discord.