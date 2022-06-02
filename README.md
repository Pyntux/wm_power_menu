Simple python + qt5 POWER MENU for WM....

Make app executable with "chmod +x wm_power_menu"

Start script (app) from any executable dir in your system.... or with ./wm_power_menu

App commands:

SHUTDOWN:"shutdown -h now"
REBOOT:"reboot"
LOGOUT:"loginctl terminate-session ${XDG_SESSION_ID-}"
SUSPEND:"systemctl suspend"
