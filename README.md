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

