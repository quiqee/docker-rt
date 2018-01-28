# Docker files

docker create --name=rutorrent \
-v <path to data>:/config \
-v <path to downloads>:/downloads \
-e PGID=<gid> -e PUID=<uid> -e TZ=<timezone> \
-p 443:443 \
-p 45566-45576:45566-45576 \
rutorrent

rutorrent page is protected with username/password: admin/admin

To change this credential (from host machine):
sudo apt-get install apache2-utils
htpasswd -c <path to data>/rutorrent/.htpasswd USERNAME
