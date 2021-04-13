# Volume mounting help

docker build -t volume-mount:v1 .

docker run -p 8080:80 --name volume-mount-v1 -d volume-mount:v1

docker run -p 8080:80 --name volume-mount-v1 -d -v /mnt/d/projects/docker/advanced-session/volume-mounting/nginx:/usr/share/nginx/html volume-mount:v1

Win directory \\wsl$\docker-desktop-data\version-pack-data\community\docker\volumes