You need to have Docker installed to run the tests

Build one of the Test-Runner images with: docker build -f [dockerfile name] -t [image-name] .

Execute the created image with: docker run --rm --name [container-name] -v "$(pwd)"/Dockerfiles:/lint-input -v "$(pwd)"/lint-output:/lint-output --user "$(id -u):$(id -g)" [image-name]

The user part is to make sure that you can delete the files created inside the container
