# Doubt
from tkinter import *
from tkinter import messagebox

root = Tk()
root.title('Tic Tac Toe - KARTIKEY')
root.iconbitmap(r'C:\Python Course\TicTacToe_gui.py')
# root.geometry("1200x710")

#X starts so true
clicked = True
count = 0

#Button Clicked Function
def b_click(b):
    global clicked, count

    if b["text"] == " " and clicked == True:
        b["text"] == "X"
        clicked = False
        count += 1

    elif b["text"] == " " and clicked == False:
        b["text"] == "O"
        clicked = True
        count += 1
    else:
        messagebox.showerror("Tic Tac Toe", "That box has already been selected\nPick another box. ")


    #Building Button
    b1 = Button(root, text = ' ', font = ("arial", 20), height = 3, width = 6, bg = "#65A8E1", command=lambda: b_click(b1)) 
    b2 = Button(root, text = ' ', font = ("arial", 20), height = 3, width = 6, bg = "#65A8E1", command=lambda: b_click(b2))
    b3 = Button(root, text = ' ', font = ("arial", 20), height = 3, width = 6, bg = "#65A8E1", command=lambda: b_click(b3))

    b4 = Button(root, text = ' ', font = ("arial", 20), height = 3, width = 6, bg = "#65A8E1", command=lambda: b_click(b4)) 
    b5 = Button(root, text = ' ', font = ("arial", 20), height = 3, width = 6, bg = "#65A8E1", command=lambda: b_click(b5)) 
    b6 = Button(root, text = ' ', font = ("arial", 20), height = 3, width = 6, bg = '#65A8E1', command=lambda: b_click(b6)) 

    b7 = Button(root, text = ' ', font = ("arial", 20), height = 3, width = 6, bg = '#65A8E1', command=lambda: b_click(b7)) 
    b8 = Button(root, text = ' ', font = ("arial", 20), height = 3, width = 6, bg = '#65A8E1', command=lambda: b_click(b8)) 
    b9 = Button(root, text = ' ', font = ("arial", 20), height = 3, width = 6, bg = '#65A8E1', command=lambda: b_click(b9)) 

        #Grid the buttons
    b1.grid(row=0, column=0)
    b2.grid(row=0, column=1)
    b3.grid(row=0, column=2)

    b4.grid(row=1, column=0)
    b5.grid(row=1, column=1)
    b6.grid(row=1, column=2)

    b7.grid(row=2, column=0)
    b8.grid(row=2, column=1)
    b9.grid(row=2, column=2)


# reset()
root.mainloop()
