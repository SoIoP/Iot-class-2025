# Exploring MQTT QoS Levels

Experiment with QoS 0, 1, and 2.
Observe how message delivery changes based on QoS settings.

## Publisher_qos.py output

```
[17:09:44] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
[17:09:44] DEBUG | Sending PUBLISH (d0, q1, r0, m1), 'b'test/qos/6510301033/temperature'', ... (5 bytes)
[17:09:44] PUBLISH REQUESTED | SID=6510301033 | temperature=25.49 | QoS=1 | msgid=1 
[17:09:44] DEBUG | Sending PUBLISH (d0, q1, r0, m2), 'b'test/qos/6510301033/humidity'', ... (5 bytes)
[17:09:44] PUBLISH REQUESTED | SID=6510301033 | humidity=42.59 | QoS=1 | msgid=2    
[17:09:44] DEBUG | Sending PUBLISH (d0, q1, r0, m3), 'b'test/qos/6510301033/pressure'', ... (7 bytes)
[17:09:44] PUBLISH REQUESTED | SID=6510301033 | pressure=1007.06 | QoS=1 | msgid=3  
[17:09:44] DEBUG | Sending PUBLISH (d0, q1, r0, m4), 'b'test/qos/6510301033/fan_speed'', ... (1 bytes)
[17:09:44] PUBLISH REQUESTED | SID=6510301033 | fan_speed=3 | QoS=1 | msgid=4       
[17:09:44] DEBUG | Received CONNACK (0, 0)
[17:09:44] DEBUG | Received PUBACK (Mid: 1)
[17:09:44] PUBLISHED | msgid=1
[17:09:44] DEBUG | Received PUBACK (Mid: 2)
[17:09:44] PUBLISHED | msgid=2
[17:09:44] DEBUG | Received PUBACK (Mid: 3)
[17:09:44] PUBLISHED | msgid=3
[17:09:44] DEBUG | Received PUBACK (Mid: 4)
[17:09:44] PUBLISHED | msgid=4
```

## Subscriber_qos.py Output

```
[17:12:50] RECEIVED | temperature: 25.11 | QoS=1
[17:12:50] DEBUG | Sending PUBACK (Mid: 1)
[17:12:50] DEBUG | Received PUBLISH (d0, q1, r0, m2), 'test/qos/6510301033/humidity', ...  (5 bytes)
[17:12:50] RECEIVED | humidity: 66.02 | QoS=1
[17:12:50] DEBUG | Sending PUBACK (Mid: 2)
[17:12:50] DEBUG | Received PUBLISH (d0, q1, r0, m3), 'test/qos/6510301033/pressure', ...  (7 bytes)
[17:12:50] RECEIVED | pressure: 1008.41 | QoS=1
[17:12:50] DEBUG | Sending PUBACK (Mid: 3)
[17:12:50] DEBUG | Received PUBLISH (d0, q1, r0, m4), 'test/qos/6510301033/fan_speed', ...  (1 bytes)
[17:12:50] RECEIVED | fan_speed: 3 | QoS=1
[17:12:50] DEBUG | Sending PUBACK (Mid: 4)
[17:12:53] DEBUG | Received PUBLISH (d0, q1, r0, m5), 'test/qos/6510301033/temperature', ...  (4 bytes)
[17:12:53] RECEIVED | temperature: 33.7 | QoS=1
[17:12:53] DEBUG | Sending PUBACK (Mid: 5)
[17:12:53] DEBUG | Received PUBLISH (d0, q1, r0, m6), 'test/qos/6510301033/humidity', ...  (5 bytes)
[17:12:53] RECEIVED | humidity: 65.12 | QoS=1
[17:12:53] DEBUG | Sending PUBACK (Mid: 6)
[17:12:53] DEBUG | Received PUBLISH (d0, q1, r0, m7), 'test/qos/6510301033/pressure', ...  (7 bytes)
[17:12:53] RECEIVED | pressure: 1012.72 | QoS=1
[17:12:53] DEBUG | Sending PUBACK (Mid: 7)
[17:12:53] DEBUG | Received PUBLISH (d0, q1, r0, m8), 'test/qos/6510301033/fan_speed', ...  (1 bytes)
[17:12:53] RECEIVED | fan_speed: 3 | QoS=1
[17:12:53] DEBUG | Sending PUBACK (Mid: 8)
Traceback (most recent call last):
```