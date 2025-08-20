# Exploring MQTT QoS Levels

Experiment with QoS 0, 1, and 2.
Observe how message delivery changes based on QoS settings.

## Publisher_qos.py output

```
d:\WORK\Year-4\IOT\Iot-class-2025-gateway\app\publisher_qos.py:20: DeprecationWarning: Callback API version 1 is deprecated, update to latest version
  client = mqtt.Client()
[15:38:09] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
Enter message to publish: [15:38:09] DEBUG | Received CONNACK (0, 0)
สสสสสสส
Enter QoS level (0, 1, 2): 2
[15:38:16] DEBUG | Sending PUBLISH (d0, q2, r0, m1), 'b'test/qos/6510301012/temperature'', ... (21 bytes)
[15:38:16] PUBLISH REQUESTED | QoS=2 | Message='สสสสสสส' | msgid=1
Enter message to publish: [15:38:16] DEBUG | Received PUBREC (Mid: 1)
[15:38:16] DEBUG | Sending PUBREL (Mid: 1)
[15:38:16] DEBUG | Received PUBCOMP (Mid: 1)
[15:38:16] PUBLISHED | msgid=1
```

## Subscriber_qos.py Output

```
d:\WORK\Year-4\IOT\Iot-class-2025-gateway\app\publisher_qos.py:20: DeprecationWarning: Callback API version 1 is deprecated, update to latest version
  client = mqtt.Client()
[15:38:09] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
Enter message to publish: [15:38:09] DEBUG | Received CONNACK (0, 0)
สสสสสสส
Enter QoS level (0, 1, 2): 2
[15:38:16] DEBUG | Sending PUBLISH (d0, q2, r0, m1), 'b'test/qos/6510301012/temperature'', ... (21 bytes)
[15:38:16] PUBLISH REQUESTED | QoS=2 | Message='สสสสสสส' | msgid=1
Enter message to publish: [15:38:16] DEBUG | Received PUBREC (Mid: 1)
[15:38:16] DEBUG | Sending PUBREL (Mid: 1)
[15:38:16] DEBUG | Received PUBCOMP (Mid: 1)
[15:38:16] PUBLISHED | msgid=1
[15:39:09] DEBUG | Sending PINGREQ
[15:39:09] DEBUG | Received PINGRESP

```