# model_application_container

pkl serialized file created using iris-classifier.ipynb
and used in flaskApi/app.py to create a Dockerfile 
and upload it to my dockerhub https://hub.docker.com/repositories/fjsoto

to run the application with docker installed:
- type: docker run -p 8080:5002 fjsoto/iris_model:v2
- open browser to localhost:8080
- upload X_test.csv file lo load values for inference 
- click submit to get data with classifications.

Now try getting it into a k8s environment.
For refrence, use files in my repo https://github.com/fjss75/k8s
