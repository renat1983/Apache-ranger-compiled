# pache-ranger-compiled

git clone https://github.com/apache/ranger.git

build in docker run -m=16g --cpus=8 -it --rm -v /opt/work:/opt/work maven:3.6.3-jdk-8 bash

change in build dir pom.xml

mvn -Pall clean -X -s /opt/work/settings.xml
mvn clean compile package install -Dmaven.test.skip=true -Drat.skip=true -Dpmd.skip=true -Dfindbugs.skip=true -Dspotbugs.skip=true -Dcheckstyle.skip=true -s /opt/work/settings.xml
