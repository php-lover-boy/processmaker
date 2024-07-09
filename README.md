# processmaker
ProcessMaker Vulnerabilites: 
# Stored Xss
1. install ProcessMaker 4 Core Docker Instance frome this repository:
https://github.com/ProcessMaker/pm4core-docker
2. this is latest pm docker version (PM_VERSION=4.1.21), below image is the .env file.
   ![image](https://github.com/php-lover-boy/processmaker/assets/111951701/6399239e-8f0b-467e-8f44-dedb21130389)
3. create a json file with xss payload.
   ![image](https://github.com/php-lover-boy/processmaker/assets/111951701/fc68a457-7ae6-4b5d-bcc0-8ed79b4a9871)
(I uploaded sample file named: sample.json)
4.Send this file to process admin user and request to import thie file as a process.
![image](https://github.com/php-lover-boy/processmaker/assets/111951701/2813e7cc-400a-4447-a8e5-1d2ae0688753)
![image](https://github.com/php-lover-boy/processmaker/assets/111951701/42c2568d-8176-4b48-a738-b71a6e7e3d53)
![image](https://github.com/php-lover-boy/processmaker/assets/111951701/97d5524c-4227-47f9-805a-d2bc402b2465)
![image](https://github.com/php-lover-boy/processmaker/assets/111951701/ff1da235-b5f3-4af4-8f06-4ac3147997dc)

5. when admin user import this file and try to archive this process, the malicious javascript code will be executed. 
![image](https://github.com/php-lover-boy/processmaker/assets/111951701/c62fdb6a-2303-46c9-8df8-6e07f617a9d5)

It is obvius that in import function there is lack of user input sanitization.

# Maliciuos file upload 




