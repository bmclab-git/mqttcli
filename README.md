# mqttcli -- MQTT Client for shell scripting
--

### 사용방법

#### pub
- mqttcli pub --conf settings.json -t "some/where" -m "your message"
- tail -f /var/log/nginx.log | mqttcli pub -t "some/where" -s

#### sub
- mqttcli sub -t "some/#"
- mqttcli sub --conf settings.json -t "some/topic"
- mqttcli sub --conf settings.json -t "some/#"

#### pub & sub
- tail -f /vag/log/nginx.log | mqttcli pubsub --pub "some/a" --sub "some/#" > filterd.log
