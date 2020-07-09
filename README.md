# ELK-Grok-filter-in-logstash-with-docker-

We have 4 log lines of GTM 

May 11 13:10:50 latone.sec alert gtmd[5901]: 011a6005:1: SNMP_TRAP: VS GTM-CUT-GTMServer-Cairo-VS (ip:port=57.55.77.5:443) (Server /Common/GTM-CUT-GTMServer-Cairo) state change red --> green
May 11 13:10:50 latone.sec alert gtmd[5901]: 011a5003:1: SNMP_TRAP: Server /Common/GTM-CUT-GTMServer-Cairo (ip=57.55.77.5) state change red --> green
May 11 13:10:50 latone.sec alert gtmd[5901]: 011ab003:1: SNMP_TRAP: Data center /Common/GTM-CUT-Datacenter-Cairo state change red --> green
May 11 13:10:50 latone.sec alert gtmd[5901]: 011a4002:1: SNMP_TRAP: Pool /Common/GTM-CUT-Pool-Cairo member GTM-CUT-GTMServer-Cairo-VS (ip:port=57.55.77.5:443) state change red --> green



We want to parse them with Grok filter in logstash and show them on elastic and kibana

# How to run:

#to make sure everything is gonna be ok
$ docker-compose up -d

#to run with docker compose
$ docker-compose up 

#you can see the elastic, kibana and logstash container is up
$ docker ps


Here is the data in elastic:

![alt text](https://github.com/RehabAbdelWahab/ELK-Grok-filter-in-logstash-with-docker/blob/master/Kibana%20output/Dev%20Tool.PNG)

Here is the search result:

![alt text](https://github.com/RehabAbdelWahab/ELK-Grok-filter-in-logstash-with-docker/blob/master/Kibana%20output/search.PNG)

Here is the bar chart in kibana:

![alt text](https://github.com/RehabAbdelWahab/ELK-Grok-filter-in-logstash-with-docker/blob/master/Kibana%20output/bar%20chart.PNG)
