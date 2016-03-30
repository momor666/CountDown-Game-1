# CountDown_Game
----------------------------------
__Theory of Algorithms__

## Project title: Word_Countdown Game
 By Haoyu Wang 
 ---------------------------
 
### Introduction

######  a Python script that solves the Countdown letters game, and a document explaining how to solver works.

###### The Countdown letters game is as detailed on Wikipedia. Esentially, you are given a list of nine random letters which contains at least three vowels and four consonants
 
###### You must find the longest possible word in the Oxford English dictionary that is an anagram of some or all of the letters in the random list.

### Language use --python (use PYQt5 to build GUI ) 

* Download library for PYQT to run this app

>- address for source : http://pyqt.sourceforge.net/Docs/PyQt5/installation.html

* reason of use PYQT to built GUi rather than original python

>- althought original pyton have package of Gui but it's limited, only have few types. I download PYQT it can design frame of app very easy and nice.

* use it

>-  Generate Ui file from this app and convert ui file to pyhon file .

### How to use this App

* Double click runMainpage.py 

* MainPage show
>![image](https://github.com/G00330443/CountDown-Game/blob/master/Graph/mainpage.PNG)
>
* Click Vowel or Consonants to generate word 
>![image](https://github.com/G00330443/CountDown-Game/blob/master/Graph/generated%20Word.PNG)

* Start time

* input answer you guessed and length of word you want to check  (word length default by 5)
>![image](https://github.com/G00330443/CountDown-Game/blob/master/Graph/inputword%20and%20set%20len%20of%20word.PNG)

* check information you need to fill then click submit
>![image](https://github.com/G00330443/CountDown-Game/blob/master/Graph/submit.PNG)
--------------------

### Python Code
* use workThread to resolve problem of  Rockon by timw time.
```python 
from PyQt5.QtCore import *

class WorkThread(QThread):
    trigger = pyqtSignal()
    def __int__(self):
        super(WorkThread,self).__init__()

    def run(self):
        for i in range(203300030):
            pass
        self.trigger.emit()  
```

* to check this word and generated word randomly
```python 
def check(word,flag,inputword) :
    cc=list(inputword)
    n=0
    flag=flag
    ww=list(word)
    for i in word :
        if i in cc :
            
            ww.remove(i)
            cc.remove(i)
        #    print(ww)
      
        if len(ww)==0 :
            break 
     
    if len(ww)==flag :
        return 0;
```
### References
* Begin Start Learn Pyqt5:   http://www.thehackeruniversity.com/2014/01/23/pyqt5-beginner-tutorial/
* Watch his video in youtube when i start doing python :https://www.youtube.com/user/onestopprogramming
