This is a small readme file about how to run the solution.

Simple run steps:
1. clone the whole repository
2. install the dependecies using the Pipfile.lock which contains all the required packages and their versions
    -$pipenv install
3. run adoption_train.py python file from the installed virtual enviroment 
4. check for a 'Goodbye' message at the bottom of your terminal after Step3
5. run adoption_predict.py python file from the installed virtual enviroment
6. open the flask_frontend.ipynb notebook an trigger the code
7. optional: try out other dog and cat combinations

Docker steps:
1. clone the repository
2. go into the cloned repository's folder
2. build docker image based on the Dockerfile
     -$docker build -t 'XY_DOCKER_IMAGE' .
3. run the docker file
    -$docker run -it --rm -p 9999:9999 'XY_DOCKER_IMAGE'
4. open the flask_frontend.ipynb notebook an trigger the code
5. optional: try out other dog and cat combinations
