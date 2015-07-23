# Mesos in one command

This is docker compose config inspired by [blog post by Sebastien Goasguen]
(http://sebgoa.blogspot.com/2015/03/1-command-to-mesos-with-docker-compose.html).

It uses official images from mesosphere and host networking to enable
interactions with tasks over real network. It also enables docker containerizer.

No state is persisted between runs so feel free to start over if you
screwed cluster state or something.

## Usage

```
docker-compose up
```

Now Mesos master should be running on port 5050; Marathon on 8080.

To kill your cluster with all the data:

```
docker-compose stop
docker-compose rm -f -v
```
