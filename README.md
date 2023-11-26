# ubuntu 


# Ubuntu 20.04 server: turn off screen until I press a key

     https://askubuntu.com/questions/1244358/ubuntu-20-04-server-turn-off-screen-until-i-press-a-key/1312193#1312193
     
    
    SOLUTION (verified with Ubuntu 20.04 server running on a laptop)
    
    Create a file:
    
    sudo nano /etc/systemd/system/enable-console-blanking.service
    And put this into the file:
    
    [Unit]
    Description=Enable virtual console blanking
    
    [Service]
    Type=oneshot
    Environment=TERM=linux
    StandardOutput=tty
    TTYPath=/dev/console
    ExecStart=/usr/bin/setterm -blank 1
    
    [Install]
    WantedBy=multi-user.target
    Then change the file rights and enable the service:
    
    sudo chmod 664 /etc/systemd/system/enable-console-blanking.service
    sudo systemctl enable enable-console-blanking.service
    And reboot the server. Now the screens blanks after 1 minute without keypresses, even before the login.

![image](https://github.com/sangbinlee/ubuntu/assets/4024414/668f8675-e82a-4c74-b4d0-336fd2c79e20)

![image](https://github.com/sangbinlee/ubuntu/assets/4024414/e4840303-f4c9-4fbe-beaf-c214101dac23)


# 우분투 서버 부팅 후 1분 후에 모니터 끄고 ssh 접속 

     1. 디비 실행
     2. next start
     
     
     root@ns1:/home/sangbinlee9/front-end/mini-do# vi docker-compose.yml
     root@ns1:/home/sangbinlee9/front-end/mini-do# docker compose up -d
     [+] Running 1/1
      ✔ Container mini-do-postgres-1  Started                                                                                                                 0.0s
     root@ns1:/home/sangbinlee9/front-end/mini-do# yarn start
     yarn run v1.22.21
     $ next start
        ▲ Next.js 14.0.3
        - Local:        http://localhost:3000
     
      ✓ Ready in 419ms



#  yarn start 백그라운드 로 실행하기 
# yarn start&

![image](https://github.com/sangbinlee/ubuntu/assets/4024414/bdb79613-c63d-464a-8693-c443192995a4)
 
![image](https://github.com/sangbinlee/ubuntu/assets/4024414/eddc2a36-9229-47b9-b0f9-4a85354fbab3)


![image](https://github.com/sangbinlee/ubuntu/assets/4024414/3e12a147-15d8-4a17-bd3f-d9fed019fd38)

![image](https://github.com/sangbinlee/ubuntu/assets/4024414/c8b0cbf4-d450-4113-b8e2-1dcca431b853)



# ubuntu
    dev set

# java -version
    sangbinlee@ns1:~$ java -version
    openjdk version "1.8.0_312"
    OpenJDK Runtime Environment (build 1.8.0_312-8u312-b07-0ubuntu1~20.04-b07)
    OpenJDK 64-Bit Server VM (build 25.312-b07, mixed mode)
    sangbinlee@ns1:~$



# java set
    $ sudo apt-get update && sudo apt-get upgrade
    $ sudo apt-get install openjdk-11-jdk


# java -version

    sangbinlee@ns1:~$ java -version
    openjdk version "11.0.13" 2021-10-19
    OpenJDK Runtime Environment (build 11.0.13+8-Ubuntu-0ubuntu1.20.04)
    OpenJDK 64-Bit Server VM (build 11.0.13+8-Ubuntu-0ubuntu1.20.04, mixed mode, sharing)


    sangbinlee@ns1:~$ sudo update-alternatives --config java
    There are 2 choices for the alternative java (providing /usr/bin/java).

      Selection    Path                                            Priority   Status
    ------------------------------------------------------------
      0            /usr/lib/jvm/java-11-openjdk-amd64/bin/java      1111      auto mode
      1            /usr/lib/jvm/java-11-openjdk-amd64/bin/java      1111      manual mode
    * 2            /usr/lib/jvm/java-8-openjdk-amd64/jre/bin/java   1081      manual mode

