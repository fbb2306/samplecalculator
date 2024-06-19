# samplecalculator
Python Project 

I use a lib. <tkinter>, with python, the calculator is very simple is a and one of my first projects, but I excited. 
I learning python. The code is below.

####################################################################################################################################



import tkinter as tk

def adicionar_numero(num):
    campo_texto.insert(tk.END, num)

def calcular():
    expressao = campo_texto.get()
    resultado = eval(expressao)
    campo_texto.delete(0, tk.END)
    campo_texto.insert(tk.END, resultado)

janela = tk.Tk()

campo_texto = tk.Entry(janela, width=50)
campo_texto.grid(row=0, column=0, columnspan=4)

botoes = [
    "7", "8", "9", "/",
    "4", "5", "6", "*",
    "1", "2", "3", "-",
    "0", ".", "=", "+"
]

row = 1
col = 0
for botao in botoes:
    tk.Button(janela, text=botao, width=12, command=lambda num=botao: adicionar_numero(num)).grid(row=row, column=col)
    col += 1
    if col > 3:
        col = 0
        row += 1

tk.Button(janela, text="Calcular", width=50, command=calcular).grid(row=row, column=0, columnspan=4)

janela.mainloop()







