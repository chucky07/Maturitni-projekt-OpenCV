# Maturitni-projekt-OpenCV
OpenCV je open-source software, který umožní práci s kamerou, obrázky a videem, sledovat objekty a primitiva a vytvořit primitiva.

Lze programovat ve více jazycích (C++, Python...)

## Postup
---
**16.9.**
* Instalace Ubuntu 16.04. ve VirtualBoxu
  - *OpenCV lze nainstalovat na Windows, Linux, Android, MacOS, FreeBSD, OpenBSD a mobily se systémem Android, Maemo, iOS. Já jsem zvolil Ubuntu, protože jsem se dočetl, že na Ubuntu je OpenCV méně problémové.*
* Instalace gcc
  - aktualní verze 6.3.0 (ověření příkazem `gcc -v`)
---  
**17.9.**
* Instalace OpenCV
  - instalace závislostí
  - *momentálně si nejsem jistý, jestli budu používat jen c++ nebo taky python, proto raději nainstaluju i python knihovny*
  - z GitHubu stáhnu OpenCV a OpenCV_contrib
  - *OpenCV_contrib je určeno k vývoji takzvaných "extra" modulů, které přispívají k funkčnosti. Nové moduly často nemají stabilní API a nejsou dobře testovány. Proto by neměli být uvolňovány jako součást oficiální distribuce OpenCV, protože se knihovna snaží udržovat dostatečný výkon, stabilitu a kompatibilitu.*
  - spuštění CMake
  - *CMake se používá ke kontrole procesu kompilace softwaru pomocí jednoduchých konfiguračních souborů nezávislých na platformě a kompilátoru a vytváření nativních makefile a pracovních prostorů, které lze použít v prostředí kompilátoru podle vašeho výběru.*
* Ověření funkčnosti OpenCV pomocí programu "displayImg.cpp"
    ```
    Mat img;    //objekt, ve kterém bude obrázek uložený
    img = imread(argv[1], CV_LOAD_IMAGE_COLOR);     //funkce "iamread" načte soubor
    namedWindow("Zobrazeny obrazek", WINDOW_AUTOSIZE);    //vytvoří okno pojmenované podle argumentu
    imshow("Zobrazeny obrazek", img);     //zobrazí obrázek uvnitř zvoleného okna  
    ```
      
    ```
   <stages>
    <_>
      <maxWeakCount>11</maxWeakCount>
      <stageThreshold>-1.2678639888763428e+00</stageThreshold>
      <weakClassifiers>
        <_>
          <internalNodes>
            0 -1 0 -4.8783610691316426e-04</internalNodes>
          <leafValues>
            5.9219348430633545e-01 -4.4163608551025391e-01</leafValues></_>
        <_>
          <internalNodes>
            0 -1 1 -4.2209611274302006e-04</internalNodes>
          <leafValues>
            3.0318650603294373e-01 -3.2912918925285339e-01</leafValues></_>
        <_>
          <internalNodes>
            0 -1 2 -4.9940118333324790e-04</internalNodes>
          <leafValues>
            4.8563310503959656e-01 -4.2923060059547424e-01</leafValues></_>
<_>
    ```
---    

**18.9.**
sudo apt install python-opencv

---

**Tvoření vlastního classifieru**
Potřebujeme hodně pozitivních a negativních snímků
  -pozitivní snímky jsou snímky, které obsahují objekt, který chceme sledovat
  -negativní snímek obsahuje


## Zajímavé odkazy 
[Videotutorial k editaci souboru README](https://www.youtube.com/watch?v=4UTSEKzsSvM)

[Instalace gcc](https://gist.github.com/application2000/73fd6f4bf1be6600a2cf9f56315a2d91) 

[Instalace OpenCV na Ubuntu](http://www.learnopencv.com/install-opencv3-on-ubuntu/)

[Zobrazení videa C++/Python](https://www.learnopencv.com/read-write-and-display-a-video-using-opencv-cpp-python/)

[Vehicle Detection Haarcascades](https://github.com/andrewssobral/vehicle_detection_haarcascades)

[Tvoření vlastního classifier](http://coding-robin.de/2013/07/22/train-your-own-opencv-haar-classifier.html)

https://github.com/mrnugget/opencv-haar-classifier-training

https://www.learnopencv.com/training-better-haar-lbp-cascade-eye-detector-opencv/

GTK2 - dev

[Screenshot v pythonu](https://gist.github.com/initbrain/6628609)

[Gstreamer video PDF](http://brettviren.github.io/pygst-tutorial-org/pygst-tutorial.pdf)

[Pyatogui screenshot](http://pyautogui.readthedocs.io/en/latest/screenshot.html)
https://stackoverflow.com/questions/44670188/gtk3-widget-mouse-events-pass-through

https://ubuntuforums.org/archive/index.php/t-1792489.html

---

http://python-gtk-3-tutorial.readthedocs.io/en/latest/builder.html

http://python-gtk-3-tutorial.readthedocs.io/en/latest/introduction.html

http://www.peteronion.org.uk/PyGobjectGtk+3/PyGtk.html

https://github.com/animeshsrivastava24/3D-SCANNER-IITB/blob/master/Root.py

https://www.root.cz/clanky/tvorba-gui-v-pythonu-s-pyside-dalsi-dostupne-ovladaci-prvky/

https://github.com/jepler/cropgui

---

## Orientační harmonogram
- Instalace VirtualBox    [hotovo]
- Instalace Ubuntu    [hotovo]
- Instalace OpenCV    [hotovo]
- Otevření obrázku a videa pomocí programu    [hotovo]
- Naprogramování softwaru pro detekci a počítání aut
- Ladění chyb

---

# Dokumentace

## OpenCV

OpenCV (Open Source Computer Vision) je knihovna funkcí, která se zaměřuje především na "počítačovou vizi." Tzn. jak počítače dokážou rozumět digitálním obrázkům nebo videu. Chceme tedy, aby počítače byly schopny toho, co lidská vizuální soustava. Data, která pomocí OpenCV získáme, můžeme poté úkládat do různých databází, grafů atd. OpneCV bylo původně vyvíjeno společností Intel a nyní je poskytováno pod open-source BSD licencí.

OpenCV je napsáno v C++ a jeho primární interface je C++. Bez problému lzve však použít také Python, Java, C# nebo Ruby. Všechny nové algoritmy jsou vyvíjeny v C++. Knihovna je multiplatformní a tak ji lze využít na Windows, Linux, macOS nebo FreeBSD.

K nejpoužívanějším algoritmům v OpenCV patří:
  - rozpoznávání obličeje
  - rozpoznávání gest
  - interakce člověk-počítač
  - mobilní robotika
  - zachycení pohybu
  - rozpoznání pohybu
  - identifikace objektů

## Haar Cascade

Haar Cascade je classifier, který používáme pro detekci objektů, pro které byl vytrénován. Classifier nejprve musíme natrénovat použitím spousty pozitivních a negativních snímků. Pozitivní snímky obsahují objekt (auto, obličej, předmět), který chceme rozpoznávat. Negativní snímky jsou snímky, které daný objekt neobsahují. Nejlépe pozadí, na kterém by se objekt mohl vyskytovat. Doporučuje se používat více negativních než pozitivních snímků s tím, že snímky budou mít stejné rozměry. Trénování probíhá na několik fází. Čím více snímků použijeme, tím déle to bude trvat, ale získáme lepší a "chytřejší" classifier. V každé fázi se pozitivní snímky náhodně přiřazují na negativní snímky a tím classifier získává přehled o tom, jak sledované objekty vypadají.

Když classifier natrénujeme, můžeme jej použít na libovolná videa nebo obrázky (samozřejmě s podporou námi napsaného programu). Classifier nám vrátí "1" pokud ve skenovaném regionu najde sledovaný objekt (v opačném případě vrátí "0"). Skenování a hledání objektu probíhá na celém obrázku.

Slovo "cascade" používáme, protože výsledný classifier je složen z jednoduších fází. Každá fáze se poté aplikuje na skenované video nebo obrázek, dokud podezřelý objekt je buď potvrzen jako sledovaný objekt nebo vyvrácen.
