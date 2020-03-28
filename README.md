This is a `docker-compose` setup to duplicate the http://longturn.net website on your computer.

# Usage

Get the code:
```
git clone --recursive https://github.com/lmoureaux/longturn-website-docker.git
cd longturn-website-docker
```

Start the website:
```
docker-compose up -d
```

The first time you start the website (or after wiping the database), you need to create the superuser:
```
docker-compose exec www python -m longturn.manage createsuperuser
```

That's it! You can point your browser to http://localhost:8000. The administrative interface is at http://localhost:8000/admin.

To shutdown, run:
```
docker-compose down
```

