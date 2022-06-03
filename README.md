## Simple python + qt5 POWER MENU for WM....


- Make app executable with "chmod +x wm_power_menu"

- Start script (app) from any executable dir in your system.... or with ./wm_power_menu


![wm_power_menu](https://raw.githubusercontent.com/Pyntux/wm_power_menu/main/wm_power_menu.png)



## App commands:

SHUTDOWN: "shutdown -h now"

REBOOT:   "reboot"

LOGOUT:   "loginctl terminate-session ${XDG_SESSION_ID-}"

SUSPEND:  "systemctl suspend"

CANCEL: just option to exit app.....


### You need to install python-pyqt5 (arch package name)

P.S. I just do not have time to make AUR package....
