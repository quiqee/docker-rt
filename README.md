# Docker files

docker create --name=rutorrent \
-v <path to data>:/config \
-v <path to downloads>:/downloads \
-e PGID=<gid> -e PUID=<uid> -e TZ=<timezone> \
-p 443:443 \
-p 45566-45576:45566-45576 \
rutorrent
