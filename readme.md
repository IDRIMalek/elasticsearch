docker run -d \
--name elasticsearch \
-p 9200:9200 \
-p 9300:9300 \
-e "discovery.type=single-node" \
elasticsearch:7.10.1

docker run -d \
        --name kibana \
        --link elasticsearch:elasticsearch \
        -p 5601:5601 docker.elastic.co/kibana/kibana:7.10.2

pip3 install elasticsearch

git config --global user.email "idri.malek@gmail.com"
git config --global user.name "IDRIMalek"
        