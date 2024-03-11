# Calculadora
Abrindo calculadora no PC
import subprocess
import sys

def open_calculator():
    if sys.platform.startswith('win'):
        subprocess.Popen('calc.exe')
    elif sys.platform.startswith('linux'):
        subprocess.Popen(['xdg-open', 'gnome-calculator'])  # Pode ser substituído pelo comando para abrir a calculadora em outras distribuições Linux
    elif sys.platform.startswith('darwin'):
        subprocess.Popen(['open', '-a', 'Calculator'])
    else:
        print("Sistema operacional não suportado.")

if __name__ == "__main__":
    open_calculator()
