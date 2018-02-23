# Setting up Play in c9.io

## Install Java 8
```
$ sudo add-apt-repository ppa:webupd8team/java
  - press enter
$ sudo apt-get update
$ sudo apt-get install oracle-java8-installer
  - enter y
  - agree to terms, enter, left arrow, enter
$ java -version
java version "1.8.0_161"
Java(TM) SE Runtime Environment (build 1.8.0_161-b12)
Java HotSpot(TM) 64-Bit Server VM (build 25.161-b12, mixed mode)
```

## Install SBT
```
$ echo "deb https://dl.bintray.com/sbt/debian /" | sudo tee -a /etc/apt/sources.list.d/sbt.list
$ sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2EE0EA64E40A89B84B2DF73499E82A75642AC823
$ sudo apt-get update
$ sudo apt-get install sbt
```
[SBT Linux Install Instructions](http://www.scala-sbt.org/1.x/docs/Installing-sbt-on-Linux.html)

## Create new Play Project
```
$ sbt new playframework/play-java-seed.g8
```
- give it a name
- skip the rest by simply pressing enter

Running
- open terminal, cd to project directory.
`$ sbt run`

Wait until you see
`[info] play.api.Play - Application started (Dev)`
Once the server is running, you can minimize the terminal window
since the application reloads automatically when you make a change.

Point your browser to http://localhost:9000

Every time you change the code, just hit refresh on your browser.


## Opening up the project in IntelliJ
1. Open IntelliJ
2. Go `File` -> `Open`
3. Navigate to the existing project folder, and open it.
4. It will say `Import Project from Gradle`, just press ok.

