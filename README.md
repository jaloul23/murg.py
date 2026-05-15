from tkinter import*
#from flutter
from tkinter import messagebox
import time
import threading
import os
import tkinter as tk
password = '6394'
def on_closing():
    messagebox.showerror('security','لي ردحسيفثوعلا عم زرب ')
def check_password():
    passo = entry.get()
    if passo == password :
        root.destroy()
        global running
        running = False 
root = Tk()
root.title('murg')
root.register(False,False)
root.attributes("-fullscreen",True)
root.resizable(False,False)
root.attributes("-topmost",True)
root.protocol("WM_DELETE_WINDOW",on_closing)
root.attributes('-alpha',0.2)
title = Label(root,text='Screen Lock',fg='white',bg='#D82148',font=('Stencil',21))
title.pack(fill=X)
label = tk.Label(root,text='أدخل كلمة المور :')
label.pack()
entry = tk.Entry(root,show='*')
entry.pack()
button = tk.Button(root,text='ي ردحسيفثوعلا عم زرب ',command=check_password)
button.pack()
root.mainloop()
