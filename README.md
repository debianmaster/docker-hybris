### docker-hybris
> This repo Explains how you can deploy SAP hybris on docker
> Most of the source and ideas are copied from https://github.com/prelegalwonder/hybris-docker
> Changed few things to make it work for myself.

### Env setup 
>  Create a docker machine for testing     

```sh
docker-machine create --virtualbox-disk-size  700000  --virtualbox-memory "4096"     -d virtualbox dev 
docker-machine start dev
eval "$(docker-machine env dev)"
111



### Build hybris image
```sh
git clone https://github.com/debianmaster/docker-hybris.git
cd docker-hybris
```

### Download hybris source zip 
> Download hybris-commerce-suite-5.4.0.4.zip   from  wiki.hybris.org   
> I saw a zip here, but i'm not sure if you can use it or not legally  https://www.swiftcore.com/repo/    at your own risk   

```sh
docker build -t "hybris" .
```

### Run hybris image
```sh
docker run -d -P hybris
```


