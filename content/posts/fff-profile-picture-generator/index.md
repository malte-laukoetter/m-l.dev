---
title: Fridays for Future Profile Picture Generator
cover: header.jpg
tags:
- fridaysforfuture
- webdev
- developersforfuture
date: 2020-04-14
lang: en

---
A profile picture generator for the Fridays for Future movement. It is used to overlay profile picture frames over images uploaded by the user to mobilize for upcoming climate strikes or other actions by Fridays for Future. It was shared and used by many activists of Fridays for Future including Greta Thunberg and Luisa Neubauer.

> Already 50 000 signatures in less than 22hrs! Read, sign & share our open letter and demands to EU- and global leaders here -> x Here you can make your own picture where you #FaceTheClimateEmergency ->x — Greta Thunberg (@GretaThunberg) July 17, 2020

This generator replaced an earlier version of such a program that required the use of a GPU-server in the backend to create these images and instead does all the processing directly in the browser of the user. This lead to a reduction of the time it takes to generate such an image between 500% and 2000% and at the same time greatly improved the privacy of the user's images as these no longer leave their device. It also supports multiple languages and nonsquare image formats.

<style>
.fff-pbg-container {
margin: 0 auto;
font-size: 16px;
}
.fff-profile-picture-generator--button-group {
margin-bottom: unset;
}
.fff-profile-picture-generator--privacy-note {
font-size: 12px;
}
.fff-profile-picture-generator--button {
display: flex;
align-items: center;
justify-content: center;
padding: 4px;
}
</style>
<div class="fff-pbg-container" style=""></div>
<script type="text/javascript" src="./profile-picture-generator.js"></script>
<script type="application/javascript">
(function () {
window.ProfilePictureGenerator({
container: document.querySelector('.fff-pbg-container'),
initialLanguage: 'de',
languages: {
de: {
name:'German',
uploadButtonTitle:"Eigenes Profilbild generieren",
downloadButtonTitle:"Profilbild herunterladen",
imageAltText:"Generiertes Fridays for Future Profilbild",
fileName:"ProfilePicture.png",
templateUrl:"./september-23-pfp-frame-fff.png",
imagePreview:"./september-23-pfp-frame-fff.png",
privacyNote:"Die ausgewählte Datei wird an keinen Server versendet. Die gesamte Bildgenerierung findet im Browser statt.",
privacyLinkText:"",
privacyLink:"",
templateRenderFunction:function(t){return[{type:"IMAGE_SQUARE",offset:0,size:Math.max(t.width,t.height),src:t.src,rotation:t.srcRotation},{type:"IMAGE_SQUARE",offset:0,size:Math.max(t.width,t.height),src:t.template,rotation:1}]}
},
en: {
name: 'English',
templateUrl:"./september-23-pfp-frame-fff.png",
imagePreview:"./september-23-pfp-frame-fff.png",
privacyLinkText:"",
privacyLink:"",
}
}
});
})();
</script>

The source code of the generator is available here: [gitlab.com/developersforfuture/profile-generator-frontend](https://gitlab.com/developersforfuture/profile-generator-frontend)

A small presentation about the generator for a university course: [Download (PDF)](generating-profile-pictures-to-help-mobilize-millions.pdf)

## Usages:

* Alle Dörfer BLEIBEN! - Lützerath bleibt 08.01.2022 - [www.alle-doerfer-bleiben.de/demo/](https://www.alle-doerfer-bleiben.de/demo/ "https://www.alle-doerfer-bleiben.de/demo/")
* Aufstand der letzten Generation - [letztegeneration.de/soli-profilbild/](https://letztegeneration.de/soli-profilbild/ "https://letztegeneration.de/soli-profilbild/")
* Bürgerrat Klima: [buergerrat-klima.de/unterstuetzen](https://buergerrat-klima.de/unterstuetzen)
* Die Grünen Würzburg: [profilbildgenerator.gruene-wuerzburg.de/](https://profilbildgenerator.gruene-wuerzburg.de/), [https://www.martin-heilig.de/am-15-maerz-gruen-waehlen/](https://www.martin-heilig.de/am-15-maerz-gruen-waehlen/ "https://www.martin-heilig.de/am-15-maerz-gruen-waehlen/")
* Fridays for Future Deutschland
  * 23. September 2022 - [fridaysforfuture.de/klimastreik/profilbildgenerator/](https://fridaysforfuture.de/klimastreik/profilbildgenerator/)
  * #AlleFür1Komma5 - [fridaysforfuture.de/allefuer1komma5/profilbild/](https://fridaysforfuture.de/allefuer1komma5/profilbild/)
  * #FaceTheClimateEmergency - [fridaysforfuture.de/facetheclimateemergency-profilbildgenerator/](https://fridaysforfuture.de/facetheclimateemergency-profilbildgenerator/)
  * #NetzstreikFürsKlima - [fridaysforfuture.de/netzstreikfursklima/profilbildgenerator/](https://fridaysforfuture.de/netzstreikfursklima/profilbildgenerator/), [pb.fridaysforfutureduesseldorf.de/](https://pb.fridaysforfutureduesseldorf.de/)
  * #KlimaWahl Bayern - [fridaysforfuture.de/bayern/profilbildgenerator/](https://fridaysforfuture.de/bayern/profilbildgenerator/)
  * #NeustartKlima - [fridaysforfuture.de/neustartklima/profilepicture-generator/](https://fridaysforfuture.de/neustartklima/profilepicture-generator/)
  * #PeopleNotProfit - [fridaysforfuture.de/reichthaltnicht/profilbildgenerator/](https://fridaysforfuture.de/reichthaltnicht/profilbildgenerator/ "fridaysforfuture.de/reichthaltnicht/profilbildgenerator/")
  * #PublicClimateSchool2020 - [studentsforfuture.info/public-climate-school/](https://studentsforfuture.info/public-climate-school/)
  * #KlimaZielStattLobbyDeal - [fridaysforfuture.de/bailout/profilbildgenerator/](https://fridaysforfuture.de/bailout/profilbildgenerator/)
  * #DanniBleibt - [fffnrw.de/dannibleibt/](https://fffnrw.de/dannibleibt/)
  * #KeinGradWeiter - [fridaysforfuture.de/keingradweiter/profilbildgenerator](https://fridaysforfuture.de/keingradweiter/profilbildgenerator)
  * Fridays for Future Düsseldorf - [fridaysforfutureduesseldorf.de/#Profilbildgenerator](https://fridaysforfutureduesseldorf.de/#Profilbildgenerator)
  * Fridays for Future Freiburg - 23. September 2022 - [freiburgforfuture.de/23-09/](https://freiburgforfuture.de/23-09/)
  * Fridays for Future Hamburg - 23. September 2022 - [fridaysforfuture.hamburg/profilbildgenerator/](https://fridaysforfuture.hamburg/profilbildgenerator/)
  * Fridays for Future Hannover - #VerkehrneuDenken - [fridaysforfuture-hannover.de/2021/08/21/nds-streik-03-09/](https://fridaysforfuture-hannover.de/2021/08/21/nds-streik-03-09/ "https://fridaysforfuture-hannover.de/2021/08/21/nds-streik-03-09/")
  * Fridays for Future Leipzig - #PeopleNotProfit - [fffleipzig.de/people-not-profit/mitmachen/#profilbildgenerator](https://fffleipzig.de/people-not-profit/mitmachen/#profilbildgenerator)
* Fridays for Future International
  * September 23rd 2022 - [fridaysforfuture.org/september23/](https://fridaysforfuture.org/september23/)
  * Fight For 1.5! - [fridaysforfuture.org/fightfor1point5/share/](https://fridaysforfuture.org/fightfor1point5/share/)
  * #FaceTheClimateEmergency - [climateemergencyeu.org](https://climateemergencyeu.org/#pbgen)
  * Fridays for Future Schweiz - [climatestrike.ch/posts/picture-generator-23-9](https://climatestrike.ch/posts/picture-generator-23-9) 
  * Fridays for Future Sweden - [profilbild.fridaysforfuture.se/](https://profilbild.fridaysforfuture.se/)
  * Fridays for Future Austria - global climate strike 25.09.2020: [fridaysforfuture.at/events/weltweiter-klimastreik](https://fridaysforfuture.at/events/weltweiter-klimastreik)
  * Młodzieżowy Strajk Klimatyczny / Fridays for Future Poland - [msk.earth/strajk-25-03](https://www.msk.earth/strajk-25-03 "msk.earth/strajk-25-03") / [fridaysforfuture.github.io/msk-march-25-pfp-gen/](https://fridaysforfuture.github.io/msk-march-25-pfp-gen/)
* hannover erneuərbar - [hannover-erneuerbar.de/unterstuetzen/profilbild](https://hannover-erneuerbar.de/unterstuetzen/profilbild)
* IG Metal Atos München - [team-igmetall-atos-muenchen.de/profilbild-2/](https://team-igmetall-atos-muenchen.de/profilbild-2/ "https://team-igmetall-atos-muenchen.de/profilbild-2/")
* JA zur StadtBahn! (Tübingen) - [jazutuebingen.de/profilbildgenerator/](https://jazutuebingen.de/profilbildgenerator/)
* Jusos Baden-Württemberg - #SPDfor1Point5 - [spdfor1point5.de/social-media/](https://spdfor1point5.de/social-media/)
* Klima vor 8 - [klimavor8.de/pbg/](https://klimavor8.de/pbg/)
* Klima-Pledge - *offline*
* Klimaliste Baden-Württemberg - *offline*
* Klimanotstand in Soest - [klimanotstand-soest.info/profilbild-generator/](https://klimanotstand-soest.info/profilbild-generator/ "https://klimanotstand-soest.info/profilbild-generator/")
* Leinemasch BLEIBT - [leinemaschbleibt.de/profilbildgenerator/](https://leinemaschbleibt.de/profilbildgenerator/)
* Nachhaltigkeitswochen @ Hochschulen BaWü - [hochschule-n-bw.de/profilbildgenerator/](https://hochschule-n-bw.de/profilbildgenerator/)
* Parents for Future Neuburg - Stadtradeln - [www.parents4future.net/en/node/3471](https://www.parents4future.net/en/node/3471)
* [Plan de Choque Social](http://www.plandechoquesocial.org/) - *offline*
* Students for Future Köln
  * FFF x LütziBleibt - [sff-koeln.de/pb-gen/](https://sff-koeln.de/pb-gen/ "https://sff-koeln.de/pb-gen/")
  * #EnteignenstattKrise - [sff-koeln.de/27-08/](https://sff-koeln.de/27-08/)
* Team Franka Bundestagswahl 2021 - [franka.jetzt/mitmachen/](https://franka.jetzt/mitmachen/ "franka.jetzt/mitmachen/")
* [#TransDayOfVisibility](https://www.change.org/p/selbstbestimmung2022-tsgabschaffen) - [fallofthepatriarchy.de/profilbild-generator/](https://fallofthepatriarchy.de/profilbild-generator/)
* [Wir sind der Osten](https://wirsindderosten.de/) - #WIRSINDEINS: [wirsindderosten.de/wirsindeins/](https://wirsindderosten.de/wirsindeins/)

Chip Article: [www.chip.de/downloads/webapp-Fridays-for-Future-Profilbildgenerator_173875366.html](https://www.chip.de/downloads/webapp-Fridays-for-Future-Profilbildgenerator_173875366.html "https://www.chip.de/downloads/webapp-Fridays-for-Future-Profilbildgenerator_173875366.html")
