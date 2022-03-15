

< JDK 1.8 설치 >




1. JDK 설치
```
 cd /home/apps/
 tar xvfz jdk-8u231-linux-x64.tar.gz
 ln -s jdk1.8.0_231 java
```


2. java 명령어 셋팅(root로 해야함)
```
 cd /usr/bin/
 rm -f java (기존에 java가 있을 경우 삭제한다.)
 ln -s /home/apps/jdk1.8.0_231/bin/java java
```


3. 환경변수 설정 (root로 해야한다.)
```
 cd /etc/
 vi profile
 (맨 밑 줄에 추가)
 JAVA_HOME=/home/apps/java
 PATH=$PATH:$JAVA_HOME/bin
 export JAVA_HOME CLASSPATH PATH
```


4. profile 추가된 환경변수 바로 적용
```
 source profile
```


5. java 설치 확인
```
 java -version
 javac -version
```

　

< Tomcat 8.0.44 설치 >



1. Tomcat 설치
```
 cd /home/apps/
 tar xvfz apache-tomcat-8.0.44.tar.gz
 ln -s apache-tomcat-8.0.44 tomcat
```


2. 환경변수 설정 (root로 해야한다.)
```
 cd /etc/
 vi profile
 (java 설정 줄에 추가한다.)
 CATALINA_HOME=/home/apps/tomcat
 PATH=$PATH:$JAVA_HOME/bin:$CATALINA_HOME/bin
 export JAVA_HOME CLASSPATH PATH CATALINA_HOME
```


3. profile 추가된 환경변수 바로 적용
```
 source profile
```


4. 톰캣 시작
```
 cd /home/apps/tomcat/bin/
 ./startup.sh
```
