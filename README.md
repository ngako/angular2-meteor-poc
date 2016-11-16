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

#### How to fix `fatal: unable to access 'https://github.com/bsliran/angular2-meteor-base/': Problem with the SSL CA cert (path? access rights?)`

1. Download the [CA certificate](https://curl.haxx.se/ca/cacert.pem) from mozilla.

2. Edit $HOME/.gitconfig file and add

```vim
[http]

    sslCAInfo=/path/to/your/cacert.pem
```

#### How to fix:
```bash
Ign https://deb.nodesource.com jessie InRelease
Ign https://deb.nodesource.com jessie Release.gpg             
Ign https://deb.nodesource.com jessie Release                 
Hit http://security.debian.org jessie/updates InRelease                      
Hit http://httpredir.debian.org jessie-updates InRelease                     
Err https://deb.nodesource.com jessie/main Sources
  
Ign http://httpredir.debian.org jessie InRelease                       
Get:1 http://security.debian.org jessie/updates/main amd64 Packages [408 kB]
Err https://deb.nodesource.com jessie/main amd64 Packages                      
  
Hit http://httpredir.debian.org jessie Release.gpg                             
Get:2 http://httpredir.debian.org jessie-updates/main amd64 Packages [17.6 kB]
Hit http://httpredir.debian.org jessie Release           
Get:3 http://httpredir.debian.org jessie/main amd64 Packages [9064 kB]
Fetched 9490 kB in 4s (2338 kB/s)   
W: Failed to fetch https://deb.nodesource.com/node_6.x/dists/jessie/main/source/Sources  

W: Failed to fetch https://deb.nodesource.com/node_6.x/dists/jessie/main/binary-amd64/Packages  

E: Some index files failed to download. They have been ignored, or old ones used instead.
```
1. Edit a file /etc/apt/sources.list.d/nodesource.list

2. Change https by http

3. Save your file and retry now.


