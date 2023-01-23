# snmpcollector-compiled-packages for raspberry pi 4 debian buster

source: https://github.com/toni-moreno/snmpcollector

## Get Code and setup example config
```
git clone https://github.com/toni-moreno/snmpcollector.git
cd snmpcollector
cp conf/sample.config.toml conf/config.toml
```
## Building the backend
```
go run build.go build           
```
## Building frontend and backend in production mode
```
npm install
PATH=$(npm bin):$PATH            # or export PATH=$(npm bin):$PATH depending on your shell
npm run build:prod               # will build fronted and backend
```
## Creating minimal package tar.gz

After building frontend and backend you wil do
```
npm run postbuild #will build fronted and backend
```
## Creating rpm and deb packages

you will need previously installed the fpm/rpm and deb packaging tools. After building frontend and backend you will do.
```
go run build.go latest
```
