# Keep back straight and drink water remind by Ubuntu notification.
-----  
## Solutions:
1. Create file water.sh
```sh
eval "export $(egrep -z DBUS_SESSION_BUS_ADDRESS /proc/$(pgrep -u $LOGNAME gnome-session)/environ)";
DISPLAY=:0 notify-send "Hey, Tran Xuan Nam" "Keep your back straight and drink water!"
```  
2. Make water.sh executable
```sh
sudo chmod +x /path/to/water.sh
```
3. Test notification
```sh
/path/to/water.sh
```
![](http://i.imgur.com/o3OSEU8.jpg)  
4. Create a job which runs every 15 minutes
```sh
*/15 * * * * /path/to/water.sh
```
5. Enjoy!
