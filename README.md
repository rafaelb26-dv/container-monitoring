## Container Monitoring

# Descrição do Projeto

Dahsboard para monitorar containers e servidores Linux

Nesse projeto temos quatro containers: 

Node Expoter -> Coleta dados do seu servidor Linux

Cadvisor -> Criado pelo google, coleta dados dos seus containers

Prometheus -> Coleta metricas através do protocolo HTTP 

Grafana -> Ferramenta apra exibir metricas através de uma interface mais interativa

Para rodar esse projeto basta usar esse comando no terminal:
"docker-compose up -d --build"


## Mão na massa


Agora precisamos adicionar os dashboards interativos no Grafana.
Vamos criar primeiro o dashboard para monitorar os Conainters:


1 -> Acesse http://localhost:3000
usuario do grafana: admin
senha: admin
![alt text](/images/Image01.png)

2 -> Clique em Add yout firt data source
Escolha o "Grafana"
![alt text](/images/Image02.png)

3 -> Em URL digite: http://localhost:9090
Em Access escolha a opção "Browser"
Vai ate o final da pagina e clique em "Save & test"
![alt text](/images/Image03.png)

4 -> Vai até a opção "+" -> Create -> Import
![alt text](/images/Image04.png)


5 -> Agora temos que adicionar o nosso dashboard
Acesse o site: https://grafana.com/grafana/dashboards/15331-docker-container-dashboard/
Clique em "Copy ID to clipeboard"
![alt text](/images/Image05.png)

6 -> Cole o ID e clique em "Load"
![alt text](/images/Image06.png)

7 -> Em "Select a Prometheus data source" escola a opção "Prometheus" e clique em "Import"
![alt text](/images/Image07.png)

E voilà temos nosso dashboarb bonitão pra monitorar nossos containers
![alt text](/images/Image08.png)



Para adicionar o Dashboard para monitorar o servidor Linux, repita os passos começando da parte "4"
Segue o link do Dashboard: https://grafana.com/grafana/dashboards/12486-node-exporter-full/

![](https://github.com/rafaelb26-dv/container-monitoring/blob/main/images/Linux.gif)

Qualquer duvida, me mandem uma mensagem no Linkedin, farei questão de responder! :)

https://www.linkedin.com/in/rafael-bastos-a53a481b6/








