import math

from pynput.mouse import Listener
x1,x2,y1,y2=0,0,0,0
sv=True



def on_click(x,y,button,pressed):
    if pressed:
        global sv,x1,x2,y1,y2
        if sv:
            x1=x
            y2=y
            sv= False
            print(" first mouse clicked  at {0} {1} with {2}".format(x,y,button))
        else:
            x2=x
            y2= y
            sv= True
            print(" second mouse clicked  at {0} {1} with {2}".format(x, y, button))
            print(f"distance {math.sqrt((x2-x1)**2+(y2-y1)**2)*0.0264583333}")


with Listener(on_click=on_click) as listener:
    listener.join()
