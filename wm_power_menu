#!/bin/env python3

from PyQt5.QtGui import *
from PyQt5.QtWidgets import *
from PyQt5.QtCore import *
import sys
import os


class MainWindow(QMainWindow):
    def __init__(self):
        super().__init__()
        self.setWindowTitle("Shutdown")
        self.setFixedSize(164, 278)
        # Prve dve cifre označavaju gde da se
        # app pojavi na ekranu X*Y. Druge dve su veličina prozora
        #self.setGeometry(850, 400, 200, 240)

        # Set Window icon
        #app_icon = QIcon()
        #app_icon.addFile('icon.ico', QSize(64, 64))
        #self.setWindowIcon(app_icon)

        # Dugme 1:
        button_1 = QPushButton("Shutdown", self)
        button_1.setGeometry(28, 20, 110, 40)
        button_1.clicked.connect(self.shutdown)

        # Dugme_2:
        button_2 = QPushButton("Reboot", self)
        button_2.setGeometry(28, 70, 110, 40)
        button_2.clicked.connect(self.reboot)

        # Dugme_3:
        button_3 = QPushButton('Logout', self)
        button_3.setGeometry(28, 120, 110, 40)
        button_3.clicked.connect(self.logout)

		# Dugme_4:
        button_4 = QPushButton('Suspend', self)
        button_4.setGeometry(28, 170, 110, 40)
        button_4.clicked.connect(self.suspend)

        # Dugme_5:
        button_5 = QPushButton('Cancel', self)
        button_5.setGeometry(28, 220, 110, 40)
        button_5.clicked.connect(self.exit)


    def shutdown(self):
        os.system("shutdown -h now")

    def reboot(self):
        os.system("reboot")

    def logout(self):
        os.system("loginctl terminate-session ${XDG_SESSION_ID-}")

    def suspend(self):
        window.hide()
        os.system("systemctl suspend")
        sys.exit()

    def exit(self):
        sys.exit()


# Aplikacija
app = QApplication(sys.argv)

# Pozivamo klasu
window = MainWindow()
# Vrlo važno, da bi prikazao prozor
window.show()

# Loop koji mora da stoji zadnji
app.exec_()
