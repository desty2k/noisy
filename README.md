
# Noisy MQTT
![build](https://github.com/desty2k/noisy/workflows/build/badge.svg)
![Docker Pulls](https://img.shields.io/docker/pulls/desty2k/noisynet)

A Python script that generates random HTTP/DNS traffic noise in the background while you go about your regular web 
browsing, to make your web traffic data less valuable for selling and for extra obscurity.

This fork supports Home Assistant MQTT integration auto discovery. After successfull connection, 
Noisy will be available as a Home Assistant switch.

![](<images/ha.jpg>)

## Run in Docker

### Using `docker run`

Run container using Docker CLI

```
docker run desty2k/noisy-mqtt -e HOST=<-UPDATE-> -e PORT=<-UPDATE-> -e USER=<-UPDATE-> -e PASSWORD=<-UPDATE->
```


### Using `docker-compose`

1. Navigate into the `noisy` directory
```
cd noisy
```

2. Update environment variables in `docker-compose.yml file`

```dockerfile
version: '3'
services:
  noisy:
    image: desty2k/noisy-mqtt:latest
    restart: "no"
    environment:
      HOST: <-UPDATE->
      PORT: 1883
      USERNAME: <-UPDATE->
      PASSWORD: <-UPDATE->

```


3. Run container using `docker-compose`
```
docker-compose up -d
```

## Authors

* **Wojciech Wentland** - *MQTT support* - [desty2k](https://github.com/desty2k)
* **Itay Hury** - *Initial work* - [1tayH](https://github.com/1tayH)

See also the list of [contributors](https://github.com/1tayH/Noisy/contributors) who participated in this project.

## License

This project is licensed under the GNU GPLv3 License - see the [LICENSE.md](LICENSE) file for details

## Acknowledgments

This project has been inspired by
* [RandomNoise](http://www.randomnoise.us)
* [web-traffic-generator](https://github.com/ecapuano/web-traffic-generator)
