# docker-compose-selenium-grid

Taken from http://www.conductor.com/nightlight/running-selenium-grid-using-docker-compose/

cd /d/Sandbox/docker/selenium_base


docker build -t selenium/base .

cd selenium_hub

docker build -t selenium/hub .

cd ..
cd selenium_firefox

docker build -t selenium/firefox .


docker-compose up -d

docker-compose scale firefox=5

 http://<boot2docker_ip>:4444/grid/console

 
docker-compose stop

docker-compose rm

##Git Cheat Sheet
https://rogerdudler.github.io/git-guide/index.de.html
