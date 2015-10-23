## Docker Distribution Stack

### Prepare to run
make sure create `/docker-data` and mount additional disk storage on this directory

### Get Started
docker-compose up -d

### Add insecure registry
add `--insecure-registry localhost -H unix:///var/run/docker.sock -H tcp://0.0.0.0:2375` to `/usr/lib/systemd/system/docker.service` 

or Ubuntu `/lib/systemd/system/docker.service`

### Docker login
`admin/password`

```
docker login localhost
cat ~/.docker/config.json
```

```json
{
	"auths": {
		"localhost": {
			"auth": "YWRtaW46cGFzc3dvcmQ=",
			"email": "deploy@docker"
		}
	}
}
```

