# WAT

Host your own helm charts using chartmuseum.

 - Includes Traefik for TLS offloading
 - Includes basic auth support


# Usage

```
cp env.example .env
```
Adjust the values to your liking

After starting the stack, you need to adjust the storage permissions [bug](https://github.com/helm/chartmuseum/issues/241#issuecomment-783167646)

```bash
docker-compose exec -u chartmuseum sh -c 'chown 1000:0 -R /charts/'
```

This needs to be done only once
