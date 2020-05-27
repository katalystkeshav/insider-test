This file consist all the steps to create docker image using the given Dockerfile and push the image to ECR repo.

1. Both Dockerfile and .dockerignore file are present in node-hello-world folder.
2. To create the docker image use the following command -

    docker build -t nodejs-test:latest .

3. To push this docker image to ECR first you have to login. For this you need AWS user credentials with required permissions.

    aws ecr get-login-password --region ap-south-1 | docker login --username AWS --password-stdin 123456789.dkr.ecr.ap-south-1.amazonaws.com

4. After the build completes, tag your image so you can push the image to this repository:

    docker tag nodejs-test:latest 123456789.dkr.ecr.ap-south-1.amazonaws.com/nodejs-test:latest

5. Run the following command to push this image to your newly created AWS repository:

    docker push 406151435945.dkr.ecr.ap-south-1.amazonaws.com/nodejs-test:latest


