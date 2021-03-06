## Kuva sõnum

--- task ---

Ava [Sense HAT-i emulaator](https://trinket.io/mission-zero){:target="_blank"} Mission Zero projekti jaoks.

Näed, et sulle on automaatselt lisatud kolm rida koodi:

```python
from sense_hat import SenseHat
sense = SenseHat()
sense.set_rotation(270)
```

![sense hat-i emulaator](images/sense-hat-emulator2.png)

See kood ühendub Astro Pi-ga ja tagab, et Astro Pi LED-ekraan kuvatakse õigesti. Jäta kood sinna, sest sul läheb seda vaja.

--- /task ---

--- task ---

Võib-olla jätaksid toreda tervituse neile ISS-i astronautidele, kes töötavad Astro Pi läheduses? Kerime sõnumit tervel ekraanil.

Lisa see rida teise koodi alla:

```python
sense.show_message("Astro Pi")
```

--- /task ---

--- task ---

Vajuta **Run** (Käivita) nuppu ja vaata sõnumit `Astro Pi` LED-ekraanil.

![näita sõnumi koodi klõpsa käivita](images/show-message-code-annotated.PNG)

--- /task ---

![Keriv sõnum](images/scroll-message.gif)

Teise sõnumi kuvamiseks kirjuta jutumärkide vahele, mida iganes sa soovid (`""`).

--- collapse ---
---
title: Milliseid tähemärke saab kasutada?
---

Sense HAT-iga saab kuvada ainult Latin 1 tähemärke, seetõttu saab kasutada ainult järgmisi tähemärke. Kõiki teisi tähemärke kuvataks nii `?`.

    +-*/!"#$><0123456789.=)(
    
    ABCDEFGHIJKLMNOPQRSTUVWXYZ
    
    abcdefghijklmnopqrstuvwxyz
    
    ?,;:|@%[&_']\~
    

--- /collapse ---

--- task ---

Samuti saad muuta ekraanil keritava sõnumi kiirust. Lisa `scroll_speed` (kerimise kiirus) olemasolevale koodireale, nagu näidatud:

```python
sense.show_message("Astro Pi", scroll_speed=0.05)
```

Sõnumi kerimise vaikekiirus on `0.1`. Numbri vähendamine muudab sõnumi kerimise kiiremaks ja numbri suurendamine muudab selle aeglasemaks.

--- /task ---