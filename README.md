# HiSynth
Am creat un mic synth ce are ca intrare un track MIDI. Informația MIDI este transformată în polifonie, având octavă, frecvență de modulație, frecvență semnal și amplitudine ajustabile fie prin interfața pluginului MAX for LIVE, fie prin OSC. Mai mult, am creat 6 preset-uri pentru a facilita interacțiunea cu synth-ul. Cel de-al șaselea preset poate fi suprascris de un preset construit de către utilizator. Întregul synth poate fi controlat atât prin interfața MAX for LIVE, cât și prin OSC.

## Instalare
Pentru folosirea acestui synth, este nevoie de Ableton Live Suite.
Se descarcă proiectul din GitHub.
Pentru controlul prin OSC, va trebui instalată aplicația de iPhone Syntien (https://apps.apple.com/ro/app/syntien/id1203153534?l=ro).

## Utilizare
Se rulează fișierul Tema5.als, ce se va deschide în Ableton Live Suite, având ca track-uri prepopulate tema principală din franciza The Pirates of the Caribbean.
Pentru controlul prin OSC, se deschide aplicația de iPhone Syntien. Se merge la Interface, unde se poate crea un nou Layout în care se vor adăuga componentele de care avem nevoie. Sugestie de Layout:

![Syntien Demo Final](https://github.com/HoriaIonita/PCON-proiect-final-Synth/assets/134622616/5f43bef7-7f95-4b17-8f5a-2c351a556e0a)

Pentru layout-ul propriu se adaugă următoarele piese:
- schimbarea octavei: incrementbox1
- generator de semnal: button1 - SIN, button2 - SAW, button3 - WAVE, iar pentru forma de undă ADSR, button4 - SAW, button5 - RECT și button6 - TRI - number of states: 1
- frecvența de modulație: rotary1 - number of states: 8
- frecvența ADSR: knob1
- amplitudine: slider1
- comutare preset-uri: button7-12 - number of states: 1
- salvare propriul preset pe poziția 6: button13 - number of states: 1
- on/off: button14 - number of states: 2

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

14.06 - Adaugare funcitonalitate completa independenta de OSC, direct in layoutul pluginului M4L

15.06 - Imbunatatire layout plugin M4L si documentatie.

![image](https://github.com/HoriaIonita/PCON-proiect-final-Synth/assets/134622616/cc3845b1-42b5-4330-8ce4-47b1eb617134)

17.06 - Adăugare funcționalitate preset.

![image](https://github.com/HoriaIonita/PCON-proiect-final-Synth/assets/134622616/43904b6e-6559-4004-aa06-1b5ce4cbd968)

18.06 - Adăugare opțiune salvare propirul preset pe varianta 6. Optimizări. Modificare aplicație OSC pentru a folosi și toate opțiunile de preset.

![image](https://github.com/HoriaIonita/PCON-proiect-final-Synth/assets/134622616/76157f32-9fec-4731-83cc-bb83f07e0839)

19.06 - Finalizare layout plugin M4L și documentație.

![image](https://github.com/HoriaIonita/PCON-proiect-final-Synth/assets/134622616/e97206c1-53cc-4da4-894d-41ec2db34da2)

## Link-uri

Trackurile MIDI - [The Pirates of the Caribbean - He is a Pirate](https://bitmidi.com/pirates-of-the-caribbean-hes-a-pirate-1-mid)
