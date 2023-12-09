# Bot_Piano_tiles
Módulo 4 - RPA - Dev aprender:  Desenvolvemos mais um bot, dessa vez, para se divertir!!! Um robô capaz de jogar o piano tiles até zerar, independente da velocidade do game.

# Construímos um bot simples 🤖
com menos de 30 linhas de código 

```ruby
import pyautogui as pg
import keyboard
import win32api
import win32con
import time

pg.click(703,390, duration=1)

def click(x,y):
    win32api.SetCursorPos((x,y))
    win32api.mouse_event(win32con.MOUSEEVENTF_LEFTDOWN, 0, 0) # segurando o botão do mouse
    time.sleep(0.05)
    win32api.mouse_event(win32con.MOUSEEVENTF_LEFTUP,0 , 0) # soltando o botão do mouse

while keyboard.is_pressed('1') == False:
    if pg.pixelMatchesColor(504,305, (0,0,0)):
        click(504,305)

    if pg.pixelMatchesColor(618,305, (0,0,0)):
        click(618,305)

    if pg.pixelMatchesColor(732,299, (0,0,0)):
        click(732,299)

    if pg.pixelMatchesColor(847,297, (0,0,0)):
        click(847,297)

```

O bot reconhece as teclas pretas e simplesmente move-se até elas, clicando-as.

![image](https://github.com/Henrique-de-Souza/Bot_Piano_tiles/assets/148600312/992e690f-6275-4f1f-afd2-638413013c47)


