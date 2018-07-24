![Website Screenshot](https://raw.githubusercontent.com/HaCSBCU/hacsbcu.github.io/gh-pages/images/readme.jpeg)

# HaCS
This is the website for HaCS - the Hackathon and Computing Society at Birmingham City University. This website acts as our central resource for content and as a playground for our members to try out new ideas and work together with others.

We're open to contributions and are always improving our site. If there are any suggestions you might have or something you'd like to work on yourself feel free to [open an issue](https://github.com/HaCSBCU/hacsbcu.github.io/issues/new).

If you are a BCU student and would like to contribute to this site but don't know how yet, it might be a good idea to drop us a message on our [Facebook group](https://www.facebook.com/groups/hacsbcu/) or drop into one of our workshops.


## Contributing
This project is targeted to society members. You are welcome to contribute issues or feature suggestions however we would prefer HaCS members take on building and implementing said features.

As this project aims to be beginner friendly, please keep a friendly, open and collaborative attitude when communicating on this repository, and be respectful of everyone's abilities and ideas.

For a full code of conduct consult our [conduct](https://github.com/hacsbcu/conduct) repository.

## Testing Locally
We're using Docker to run the site locally for testing purposes. You'll need to go [here](https://hub.docker.com) and create an account to download Docker. To run the site with Docker, you'll need to create a Docker image, and then create a container using that image.

To create the image, run
```
docker build -t hacs .
```

To run a container using this image, run
```
docker run -d -p 3000:80 --name hacs hacs
```

Then navigate to [http://127.0.0.1:3000](http://127.0.0.1:3000), or whatever port you used in the above command.

Every time you make changes to the source code, you'll have to rebuild the image and re-run the container. To rebuild the image, run
```
docker rmi hacs -f
``` 

To re-run the container, run
```
docker rm hacs -f; docker run -d -p 3000:80 --name hacs hacs
```