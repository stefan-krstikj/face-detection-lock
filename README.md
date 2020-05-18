#Launch Command:
`
python3 webcam_cv3.py
`
##ВАЖНО:
#Odkako ke go klonirate repo-to, treba da gi izvrsite slednite komandi za da go zemete LCD Driver-ot, bidejki driverot e vsusnost zemen od drugo repo na drug github (ova moze da se napravi i so COPY-PASTE NA NEGOTOVOTO REPO, no github pravi problemi i ovoj nacin e 'pravilniot')
```
cd TempName
(mozno e da treba i cd opencv-face-recognition, probajte prvo bez)
git submodule init
git submodule update
```

Potrebno e da imate pip / pip3 i da gi instalirate slednite
```
pip3 install opencv-python
pip3 install imutils
pip3 install smbus
pip3 install numpy
sudo apt-get install python3-smbus
```

Potrebno e odkako ke go klonirate submodule-ot da smenite vo prvite linii vo *lcddriver.py*
```
from lcd import i2c_lib

ADDRESS = 0x3f
```


# TempName

##TODO
1. openCV so python sto raboti na laptop kamera ✓
2. prefrlanje na programot na Raspberry Pi 
3. kupuvanje na eksterna USB kamera
4. Voveduvanje na NFC tag
5. dopolnitelni raboti koga ke imame vreme

