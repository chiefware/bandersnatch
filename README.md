# bandersnatch

#bandersnatch writes default to /srv/pypi so start docker and mount it: 
docker run --detach --privileged  -ti -e "container=docker" --name=bandersnatch -v /sys/fs/cgroup:/sys/fs/cgroup -v /c/Users/<your user>/pypi:/srv/pypi chiefware/bandersnatch
#to start mirror run:
docker exec bandersnatch bash -c 'bandersnatch mirror'
# if you behind proxy  docker exec bandersnatch bash -c 'export https_proxy=http://<proxy-user>:<proxy-password>@<your proxywebadrees>:<proxy portnumber>;bandersnatch mirror'
