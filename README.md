docker-syncthing
================

[Syncthing](http://syncthing.net/) Docker image

### How to run

With docker:

	docker run -d \
		--name syncthing \
		-p 8080:8080 -p 22000:22000 -p 21025:21025/udp \
		-v /opt/docker/syncthing/config:/home/syncthing/.config/syncthing \
		-v /opt/docker/syncthing/Sync:/home/syncthing/Sync \
		romqin/syncthing


Or docker-compose:
	
	app:
		image: romqin/syncthing
		ports:
		- "8080:8080"
		- "22000:22000"
		- "21025:21025/udp"
		volumes:
		- ./config:/home/syncthing/.config/syncthing
		- ./data:/home/syncthing/data

Then access Syncthing Web UI at [http://localhost:8080/]()
