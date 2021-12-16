# Simple GUI Calulator in python


import tkinter as tk

root=tk.Tk()
def click(event):
    global str
    text=event.widget.cget("text")
    print(text)
    if text=="=":
        if str.get().isdigit():
            value=int(str.get())
        else:
            value=eval(screen.get())
            str.set(value)
            screen.update()
    elif text=="c":
        str.set("")
        screen.update()
    else:
        str.set(str.get()+text)
        screen.update()


# setting the windows size
root.geometry("350x560")
root.title("Calculator by Soni")
str=tk.StringVar()
str.set("")
screen=tk.Entry(root,textvariable = str, font=('calibre',20,'normal'))
screen.pack(fill = tk.X, ipadx=8,pady=10,padx=10)
#set number on button
f=tk.Frame(root,bg="grey")
b=tk.Button(f,text="9",padx=15,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=20,pady=12)
b.bind("<Button-1>",click)
b=tk.Button(f,text="8",padx=15,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=20,pady=12)
b.bind("<Button-1>",click)
b=tk.Button(f,text="7",padx=15,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=20,pady=12)
b.bind("<Button-1>",click)
f.pack()
f=tk.Frame(root,bg="grey")
b=tk.Button(f,text="6",padx=15,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=20,pady=12)
b.bind("<Button-1>",click)
b=tk.Button(f,text="5",padx=15,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=20,pady=12)
b.bind("<Button-1>",click)
b=tk.Button(f,text="4",padx=15,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=20,pady=12)
b.bind("<Button-1>",click)
f.pack()


f=tk.Frame(root,bg="grey")
b=tk.Button(f,text="3",padx=15,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=20,pady=12)
b.bind("<Button-1>",click)
b=tk.Button(f,text="2",padx=15,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=20,pady=12)
b.bind("<Button-1>",click)
b=tk.Button(f,text="1",padx=15,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=20,pady=12)
b.bind("<Button-1>",click)
f.pack()

f=tk.Frame(root,bg="grey")
b=tk.Button(f,text="0",padx=17,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=20,pady=12)
b.bind("<Button-1>",click)
b=tk.Button(f,text="-",padx=17,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=20,pady=12)
b.bind("<Button-1>",click)
b=tk.Button(f,text="*",padx=17,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=20,pady=12)
b.bind("<Button-1>",click)
f.pack()

f=tk.Frame(root,bg="grey")
b=tk.Button(f,text="/",padx=15,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=20,pady=12)
b.bind("<Button-1>",click)
b=tk.Button(f,text="%",padx=15,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=20,pady=12)
b.bind("<Button-1>",click)
b=tk.Button(f,text="=",padx=15,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=20,pady=12)
b.bind("<Button-1>",click)
f.pack()

f=tk.Frame(root,bg="grey")
b=tk.Button(f,text="Clear",padx=8,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=18,pady=12)
b.bind("<Button-1>",click)
b=tk.Button(f,text="+",padx=8,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=18,pady=12)
b.bind("<Button-1>",click)
b=tk.Button(f,text=".",padx=8,pady=4,font="lucida 25 bold")
b.pack(side=tk.LEFT,padx=18,pady=12)
b.bind("<Button-1>",click)
f.pack()


root.mainloop()
