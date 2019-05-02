# sshfs with caddy files

~~~
#ex:
docker run -it --rm \
  -p 2015:2015 \
  --cap-add SYS_ADMIN \
  --device /dev/fuse \
  --name sshfs \
  -e UID=1000 \
  -e GID=100 \
  -e IDENTITY_FILE=/config/id_rsa\
  -v $$PWD/config:/config \
  -v $$PWD/mnt:/srv \
  v20100/caddy-sshfs \
  id@sshfsserver.com:/ac/ish/archives-videos/projet-0001
~~~
