# Reverse proxy against remote

Will target TLS port og www.nrk.no (see [haproxy.cfg](haproxy.cfg)) 

    docker build -t reverse-haproxy .
    docker run -d -p443:443 --name reverse-haproxy reverse-haproxy
    docker ps
    curl -vvv -k https://localhost:443
    docker stop reverse-haproxy
