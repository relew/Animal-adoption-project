# This is a small readme file about how to run the solution.

# Simple run steps:
1. clone the whole repository
2. install the dependencies using the Pipfile.lock which contains all the required packages and their versions
    -$pipenv install
3. run adoption_train.py python file from the installed virtual environment  
4. check for a 'Goodbye' message at the bottom of your terminal after Step3
5. run adoption_predict.py python file from the installed virtual environment 
6. open the flask_frontend.ipynb notebook and trigger the code
7. optional: try out other dog and cat combinations

# Docker steps:
1. clone the repository
2. go into the cloned repository's folder
2. build docker image based on the Dockerfile
     -$docker build -t 'XY_DOCKER_IMAGE' .
3. run the docker file
    -$docker run -it --rm -p 9999:9999 'XY_DOCKER_IMAGE'
4. open the flask_frontend.ipynb notebook and trigger the code
5. optional: try out other dog and cat combinations

# Cloud Deployment steps(with docker only):

1. clone the repository
2. go into the cloned repository's folder
3. set up the aws environment using the following bash commands:
    -pipenv install awsebcli --dev (install aws elastic beanstalk service)
    -pip init -p docker -r eu-west-1 'XY-serving' (-p stands for the platform and we are using a docker platform now, -r stands for the region)
    -eb local run --port 9999 (if you want to test the solution locally -> same results as a simple docker run)
    -eb create 'XY-env' (to create and open an active environment for the solution)
        -at the bottom of the automatic message you will see a line starting as "Application available at 'XY-env.....'
        -this 'XY-env.....com' will be the open url provided by amazon where you can test the solution
 4. open the flask_frontend.ipynb notebook and trigger the code using the aws url('http://XY-env......elasticbeanstalk.com/adoption_predict')
 5. optional: try out other dog and cat combinations
