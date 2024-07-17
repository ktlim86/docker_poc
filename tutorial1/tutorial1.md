# Instruction

Build an airflow image from scratch

1. Build the image by running the command `docker build -f tutorial1/Dockerfile -t "<<LOGIN>>/<<IMAGE_NAME>>" .`, where `<<LOGIN>>` is the account you use to login to Docker Hub and `<<IMAGE_NAME>>` is the name of the image you want to give. 
2. Then run the image by `docker run -it --name "test" -it --rm <<LOGIN>>/<<IMAGE_NAME>> sh` .
3. Do a `docker login` to login to the Docker Hub account.
4. Lastly, do a `docker push <<LOGIN>>/<<IMAGE_NAME>>`.