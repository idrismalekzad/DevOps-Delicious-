# DevOps-Delicious
How To Install Prometheus and Grafana In Your Windows or Linux System 

Windows :
1- first of all be sure that you installed docker daemon in your system (in windows you can do it with installing Docker Desktop)

2- after that you shold place the prometheus.yml and Grafana.ini in a specail place in your system 
    -  volumes:
      - E:/Sohail/Amoozesh/DEVOPS/Traine-Doc/PrometheusConfigs/prometheus.yml:/etc/prometheus/prometheus.yml                 (Line 53 in docker-compse.yml)
    -  volumes:
      - E:/Sohail/Amoozesh/DEVOPS/Traine-Doc/GrafanaConfigs/grafana.ini:/etc/grafana/grafana.ini  
for example here is a part of my docker compose file that you can see them in the repository . now take a look to this addresses                    (Line 84 in docker-compse.yml)
E:/Sohail/Amoozesh/DEVOPS/Traine-Doc/PrometheusConfigs/prometheus.yml and
E:/Sohail/Amoozesh/DEVOPS/Traine-Doc/GrafanaConfigs/grafana.ini 
here is the locations that the (prometheus.yml and Grafana.ini) must be placed (this location is desired but make attention if you place the files in your desired locations so you must change the docker compose file address as your placed location !!!)
for example if your location is (D:/User/config) => so the docker compse file will be changed to 
    -  volumes:
      - D:/User/config/prometheus.yml:/etc/prometheus/prometheus.yml
    -  volumes:
      - D:/User/config/grafana.ini:/etc/grafana/grafana.ini  
      

3- after that now you should run the CMD or PowerShell in the docker-compose file Location and run this command 
  => dokcer-compose up -d
4- after That the Prometheus will be available in http://localhost:9090/ and Grafana wil be available in http://localhost:3000/ 

 
