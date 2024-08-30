This is the overall plan , I will Clone a website repo from github into my machine , then create an images from it using DockerFile , then running a container and testing it from my localmachine
Then I will create a docker images from the website and push it to the DockerHub 
Then I will pull the image from my EC2 CLI , and running a container On it finally accessing the website from the EC2 public Ip again !

![Capture d'écran 2024-08-30 132454](https://github.com/user-attachments/assets/074a8180-02e1-4c5e-be29-675269d4257a)

First : Clone the Website from github 

![Capture d'écran 2024-08-30 141529](https://github.com/user-attachments/assets/6b40d107-3b5b-4040-9f97-6e43a062ba6b)

*Verifying Its content* 

![Capture d'écran 2024-08-30 141621](https://github.com/user-attachments/assets/fbdb1ba3-fc54-4604-abc2-d4fa43d90c9c)

Building Image from the Website , using Dockerfile : 

![Capture d'écran 2024-08-30 141851](https://github.com/user-attachments/assets/46b67dfa-7234-4ba0-8e66-f5b7f0f4dfb7)

![Capture d'écran 2024-08-30 142855](https://github.com/user-attachments/assets/0931ac33-29c3-4ec3-b92b-9990b0cee465)

![Capture d'écran 2024-08-30 142908](https://github.com/user-attachments/assets/32a263bf-89e8-4b0b-b959-dbf9b5e6d6f5)

Running the Container from the image and testing it on local machine :

![Capture d'écran 2024-08-30 142928](https://github.com/user-attachments/assets/af1137d0-4f9f-4afd-9d5c-e575cf2e99fd)

![Capture d'écran 2024-08-30 143111](https://github.com/user-attachments/assets/a74c51e7-30c0-4208-b53e-fad64ad27f80)

*Exposed via port 3000*

![Capture d'écran 2024-08-30 144950](https://github.com/user-attachments/assets/458b9890-c740-4591-960b-4503f180fe56)

*Website Working*

Now , we will commit the container to create an image from It and push it to the dockerHub :

First thing to do is connect to Docker :

![Uploading Capture d'écran 2024-08-30 143844.png…]()

*commit* 


![Capture d'écran 2024-08-30 145646](https://github.com/user-attachments/assets/0786efcd-d23a-4249-bf60-fcc2176a6359)


*Pushing to dockerHub * 

![image](https://github.com/user-attachments/assets/25da3915-5e73-4f92-947c-3faad650f3e3)

*Verify On Docker Desktop * 


![image](https://github.com/user-attachments/assets/00212d5a-e6d3-4bad-829e-3cc4554e50a4)


Since the image is on DockerHub and Public , we will login to our EC2 instance and pull it then run it : 


![image](https://github.com/user-attachments/assets/3558888c-4f23-45a5-8a5d-be1cf4dd3d00)

We will run it and expose it through another Port "4000" : 


![image](https://github.com/user-attachments/assets/b7a993ca-8160-4cd8-afea-bf9c2ed620b7)


Now , we will acces the website with EC2 public ip : 


![image](https://github.com/user-attachments/assets/5be7c5b8-9fe7-4a94-a5f6-a18f61cd4ea2)

*WebSite Working on AWS*

![image](https://github.com/user-attachments/assets/7202a0e5-4f3c-4d1c-a5c1-0bd4ebd77b37)



