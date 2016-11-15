# angular2-meteor-poc
A simple POC to show how to use angular2 with meteor: An open source platform for web, mobile, and desktop.

### How you can launch it?

```sh
docker run -it --name <name-container> -e LOCAL_USER_ID=`id -u $USER` -p 3000:3000 -v $PWD/src:/home/dev/src -e LOCAL_USER_NAME=$USER -d ngako/npm
```
