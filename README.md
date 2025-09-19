# glcdfont_GR-for-YoRadio
Η βιβλιοθήκη Adafruit_GFX δεν υποστηρίζει Unicode. 
Επομένως, για να εμφανίσουμε ελληνικούς χαρακτήρες Unicode, πρέπει:
1) Να αλλάξουμε τη γραμματοσειρά Arduino/libraries/Adafruit_GFX_Library/glcdfont.c
2) Να γράψουμε μια συνάρτηση μετατροπής unicode σε ascii για τα ελληνικά.
   Ένα παράδειγμα μιας τέτοιας συνάρτησης για τη ρωσική γλώσσα υπάρχει στο αρχείο 
   yoRadio/src/displays/tools/utf8RusGFX.h, οπότε σε αυτό κάνουμε τις απαραίτητες 
   προσθήκες για την εμφάνιση των ελληνικών χαρακτήρων.

Τα αρχεία από αυτό το ZIP έχουν τις απαραίτητες αλλαγές για υποστήριξη ελληνικών 
και πρέπει να αντιγραφούν στις ακόλουθες τοποθεσίες:
1) displayL10n_custom.h ----> yoRadio\locale
2) glcdfont.c           ----> \Arduino\libraries\Adafruit_GFX_Library
3) utf8RusGFX.h         ----> yoRadio\src\displays\tools
4) myoptions.h        ----> change to RU  as you saw ----> #define L10N_LANGUAGE     RU

Το αρχείο "Ελληνικοί χαρακτήρες.docx" δείχνει τους χαρακτήρες που περιέχει το 
τροποποιημένο αρχείο glcdfont.c
