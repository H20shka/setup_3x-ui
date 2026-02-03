# Script-for-preparation-server-for-VPN
Hello!
It's a script which install all what u need for make a VPN.
How to use:

1. Copy the file to the server (for example, via SCP or SFTP):

 
 scp setup_3xui.sh user@yourserver:/path/to/setup_3xui.sh
 

2. Make it executable on the server(if not done):


 chmod +x setup_3xui.sh


3. Run the script(with root or sudo privileges):

 bash sudo ./setup_3xui.sh 

 What the script does:

- Updates packages
- Install Git and Docker
- Clones 3x-ui from GitHub
- Switches to v1.4.6 version
- Runs 3x-ui in the background via Docker Compose
- Outputs instructions for accessing the panel

 Warnings:

- Run on Ubuntu/Debian server
- Make sure that ports 2053 are open in the firewall
 - After installation, the panel is available at http://yourserverip:2053/panel/
