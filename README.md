<img width="579" alt="image" src="https://github.com/user-attachments/assets/674a01f0-fdf5-4e21-9ac4-a96a9a281bc7">Deploy Microservice on AWS EC2 
————————————————
 
[ec2-user@ip-172-31-29-187 ~]$ sudo su
[root@ip-172-31-29-187 ec2-user]# yum update -y
[root@ip-172-31-29-187 ec2-user]# yum install httpd -y
[root@ip-172-31-29-187 ec2-user]# 	service httpd start
[root@ip-172-31-29-187 ec2-user]# yum install docker 
[root@ip-172-31-29-187 ec2-user]# service  docker start 

rsync -avz -e "ssh -i tempkey.pem" SpringBootProductService1/ ec2-user@3.111.38.50:/home/ec2-user/
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo yum install python3-pip
 docker-compose --version

docker pull postgres:13
 docker image build -t product-service .

1. Connect to Ec2 with tempkey.pem from ~/Downloads/Awstest
<img width="782" alt="image" src="https://github.com/user-attachments/assets/7fe9a3ff-11a7-4b56-9e94-1ec4fa553247">


2.  Install Docker - yum install docker
3. > service docker start
   > <img width="579" alt="image" src="https://github.com/user-attachments/assets/433c46b6-d3a0-4b31-8c74-749be37ee63b">

4. Local and copy the project to /home/ec2-user

a  rsync -avz -e "ssh -i tempkey.pem" SpringBootProductService1/ ec2-user@3.111.38.50:/home/ec2-user/
   <img width="1062" alt="image" src="https://github.com/user-attachments/assets/bd90927e-dbfd-45c0-9ef5-a8c8ef47b2dc">
5.  Install docker-compose
- [ ] sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

* sudo chmod +x /usr/local/bin/docker-compose

* <img width="893" alt="image" src="https://github.com/user-attachments/assets/c065560c-b627-4e3e-8753-5cb523edb179">

4. Build image of Postgres’s 
*  ec2-user]# docker pull postgres:13
*  <img width="685" alt="image" src="https://github.com/user-attachments/assets/92aef083-6f14-4810-8eea-94a072c4702f">

6. Build image of product-service
[root@ip-172-31-1-208 ec2-user]# docker image build -t product-service .
<img width="813" alt="image" src="https://github.com/user-attachments/assets/4aac3fa1-7211-4df4-ac2f-96cf36f4442f">

* [root@ip-172-31-1-208 ec2-user]# docker-compose up
* <img width="1053" alt="image" src="https://github.com/user-attachments/assets/03336298-6ce3-4cfb-8cc7-0f4ec0e640fa">









   
