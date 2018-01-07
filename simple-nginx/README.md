# simple-nginx

Build the docker image by `docker build -t hoanhan/nginx .`

Run the container using: 
```
docker run -d -p 80 --name website -v $PWD/website:/var/www/html/website hoanhan/nginx nginx
```
- In the config file, we set `daemon off`. Therefore, we pass the `nginx` command to `docker run` so it can run interactively in the foreground.
- We mount, as a volume, the directory `$PWD/website` to `/var/www /html/website` in our container.
- When we edit `index.html`, change will apply immediately when we `curl` it again.
