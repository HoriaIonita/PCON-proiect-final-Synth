# Synth Hi
Am creat un mic synth ce are ca intrare un track MIDI. Informația MIDI este transformată în polifonie, având octavă, frecvență de modulație, frecvență semnal și amplitudine ajustabile fie prin interfața pluginului MAX for LVIE, fie prin OSC.

## Instalare
Pentru folosirea acestui synth, este nevoie de Ableton Live Suite.
Se descarcă proiectul din GitHub.
Pentru controlul prin OSC, va trebui instalată aplicația de iPhone Syntien (https://apps.apple.com/ro/app/syntien/id1203153534?l=ro).

## (Utilizare)
Se rulează fișierul Tema5.als, ce se va deschide în Ableton Live Suite, având ca track-uri prepopulate tema principală din franciza The Pirates of the Caribbean.
Pentru controlul prin OSC, se deschide aplicația de iPhone Syntien. Se merge la Interface, unde se poate crea un nou Layout. Sugestie de Layout:
![Syntien Demo](https://github.com/HoriaIonita/PCON-proiect-final-Synth/assets/134622616/341811a4-db2b-4b5d-94cd-538bed6d6144)

## Istoric

16.03 - Am facut mai multe tipuri de generator de semnal si am incercat sa le fac usor de interschimbat pentru a se observa diferentele. Am adaugat si un osciloscop ca sa avem si o reprezentare vizuala a semnalelor. Am implementat un generator de note random prin alta metoda decat cea de la keyboard. Am ajuns la multiple posibilitati de a conecta fiecare parametru, in final ajungand la un fel de sintetizator partial util si foarte interesant.

![Tema 1](https://github.com/HoriaIonita/PCON-proiect-final-Synth/assets/134622616/3665ddfe-9f84-40ff-8d37-51fd417039be)

23.03 - Am facut 3 tipuri de semnale continue care sa modifice parametrii ADSR, fiind foarte usor de comutat intre optiuni, avand o frecventa variabila printr-un slider. Am reintrodus generatorul random de melodie pe care l-am folosit si in tema trecuta, ceea ce face ca micul nostru sintetizator sa aiba deja destul de multe optiuni, atat de transpunere, modulatie, cat si ajustare a tuturor frecventelor diferitelor semnale si modificare a parametrilor dinamica. Am creat o modalitate de a face amplitudinea variabila prin mai multe mijloace. Prin legarea la generatorul melodiei de note random, micsoram periodic aplitudinea, iar prin ”metro 250” facem ca modificarile sliderului sa ia efect mai repede decat schimbarile notelor. Astfel am obtinut atat un efect sonor interesant, cat si un mini sintetizator versatil.

![Tema 2](https://github.com/HoriaIonita/PCON-proiect-final-Synth/assets/134622616/1124e96e-9b14-4b1c-83c5-c673abab60fa)

30.03 - Am facut imbunatatiri, de data asta lucrand cu poly~, pack/unpack, si p + inlet. Am generat melodie random si m-am folosit de MIDI, am facut generare pe saw, rect si tri pentru ADSR.

![Tema 3](https://github.com/HoriaIonita/PCON-proiect-final-Synth/assets/134622616/11ab060f-fafc-4766-8988-0fcff87ae6d6)

06.04 - Am creat o interfata custom pe telefon pentru a controla sintetizatorul din temele trecute, avand 3 slidere: unul controleaza tempo de la melodia generata random, al doilea controleaza octava in care se genereaza melodia, iar al treilea controleaza amplitudinea semnalului de iesire. Am pus 6 butoane pentru a comuta semnalul generat si formele de unda de la ADSR, plus inca unul care porneste/opreste sintetizatorul (practic opreste generarea melodiei, dar si difuzorul). Am mai adaugat un rotary cu care comut intre cele 8 frecvente de modulatie, si in abstract un knob cu care modific frecventa de generare a semnalelor de la ADSR.

![Tema 4 Horia Ionita](https://github.com/HoriaIonita/PCON-proiect-final-Synth/assets/134622616/35e65369-8878-49fc-8997-ca552db2fe4c)
	
20.04 - Am facut un Instrument MAX for LIVE, reusind sa ma folosesc de un track MIDI ca input pentru synth (track-ul 3; track-urile 1 si 2 au un grand piano pe ele). Synthul este controlat prin semnale OSC de pe telefon.

![Tema 5](https://github.com/HoriaIonita/PCON-proiect-final-Synth/assets/134622616/00b66aac-b60e-463f-812a-a5128d177e88)

10.05 - Adaugare schimbare de octava.

![Varianta finala, din inregistrarea video](https://github.com/HoriaIonita/PCON-proiect-final-Synth/assets/134622616/17dda93a-782a-4f69-bc09-da5a339d0b06)



## Link-uri

Trackurile MIDI - The Pirates of the Caribbean - He is a Pirate - [...](https://bitmidi.com/pirates-of-the-caribbean-hes-a-pirate-1-mid)

# Dezvoltarea proiectului

Pentru început:

1. Creează-ți cont pe Github
2. Download și install [Github Desktop](https://desktop.github.com/)
3. Citește [acest ghid](https://charlesmartin.com.au/blog/2020/08/09/student-project-repository) și ține la îndemână [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet).

Apoi, procesul este următorul (inspirat de [aici](https://cs.anu.edu.au/courses/comp1720/deliverables/05-major-project/#submission-process)):

1. *fork* al acestui template către propriul tău cont de Github

![](assets/fork.gif)

_(dacă preferi cumva ca repo-ul să nu fie vizibil de către public, îl poți seta ca Private din Settings - "Change visibility". Atunci trebuie să mă adaugi drept colaborator, ca eu să am acces.)_

2. *clone* al repo-ului din Github Desktop pentru a-l downloada local

![](assets/clone.gif)

3. *commit* și *push* pe măsură ce lucrezi la proiect. Ultima versiune push-ată pe server înainte de deadline va conta pentru evaluare.

![](assets/commit.gif)

## Elemente obligatorii

1. Acest readme completat. Titlu, descriere, mod de utilizare, istoric, link-uri utile.

   Poți include și imagini și chiar [gif-uri animate](https://www.screentogif.com/), sau link-uri către materiale audio/video.
   
   Vezi [aici](https://charlesmartin.com.au/blog/2020/08/09/student-project-repository) mai multe sugestii.

2. [Declarația de originalitate](statement-of-originality.yml) completată. Tot ce nu este inclus acolo va fi considerat 100% contribuție proprie.

    *(formatul este adaptat de [aici](https://gitlab.cecs.anu.edu.au/comp1720/2018/comp1720-2018-major-project/-/blob/master/statement-of-originality.yml). Da, este un pic ironic să refolosim un doc [de altundeva](https://cs.anu.edu.au/courses/comp1720/resources/faq/#how-do-i-fill-out-my-statement-of-originality), dar menționăm sursa deci nu este plagiat!)*

3. Proiectul în sine. Tot codul trebuie să fie prezent, proiectul trebuie să poată rula conform instrucțiunilor din readme. Dacă e nevoie de asset-uri mari (sunete, video etc), [folosește Git LFS](https://git-lfs.github.com/) sau include link de download în instrucțiunile de instalare.

