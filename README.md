# bandersnatch

bandersnatch writes default to /srv/pypi so start docker and mount it: 
docker run --detach --privileged  -ti -e "container=docker"  -v /sys/fs/cgroup:/sys/fs/cgroup -v /c/Users/<your user>/pypi:/srv/pypi -p 52022:22 chiefware/bandersnatch
to start mirror run in container:
bandersnatch mirror
