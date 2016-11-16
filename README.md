# angular2-meteor-poc
A simple POC to show how to use angular2 with meteor: An open source platform for web, mobile, and desktop.

### How you can launch it?

```bash
docker run -it --name <name-container> -e LOCAL_USER_ID=`id -u $USER` -p 3000:3000 -v $PWD/src:/home/dev/src -e LOCAL_USER_NAME=$USER -d ngako/npm
```

### Mistakes

#### How to fix `curl: (60) SSL certificate problem: unable to get local issuer certificate` ?

1. Download the [CA certificate](https://curl.haxx.se/ca/cacert.pem) from mozilla.

2. Edit $HOME/.curlrc file and add `cacert=/path/to/your/cacert.pem`

#### How to fix
```
fatal: unable to access 'https://github.com/bsliran/angular2-meteor-base/': Problem with the SSL CA cert (path? access rights?)
```

1. Download the [CA certificate](https://curl.haxx.se/ca/cacert.pem) from mozilla.

2. Edit $HOME/.gitconfig file and add

```
[http]

    sslCAInfo=/path/to/your/cacert.pem
```


