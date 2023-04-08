# devops-course-lab3

1. Building image
   Go to folder with Dockerfile and to build your image run the following command:
   docker build . -t node-app 
   
2. Tag your image 
   docker tag <image id> <your username>/node-app:latest
   (command that I used: docker tag 02799ef4419e tchernova/node-app:latest 

3. Push image 
   docker push tchernova/node-app

4. Run it with parameters:
   -p means port mapping
   -d run container in a deamon mode
   --cpu-period define cpu period
   --cpu-quota define cpu quota
   --memor define memory limits
   
   docker run -p 80:8080 -d --cpu-period=50000 --cpu-quota=25000 --memory=512m  tchernova/node-app

5. See the running containers list 
   docker ps
