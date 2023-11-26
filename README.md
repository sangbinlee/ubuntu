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

