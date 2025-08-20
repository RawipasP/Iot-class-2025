# Exploring MQTT QoS Levels

Experiment with QoS 0, 1, and 2.
Observe how message delivery changes based on QoS settings.

## Publisher_qos.py output

```
c:\Users\FDT-CDTI\Documents\IOT\Iot-class-2025-gateway\app\publisher_qos.py:20: DeprecationWarning: Callback API version 1 is deprecated, update to latest version
  client = mqtt.Client()
[15:32:08] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
[15:32:08] DEBUG | Received CONNACK (0, 0)
Enter message to publish: Hello
Enter QoS level (0, 1, 2): 2
[15:32:17] DEBUG | Sending PUBLISH (d0, q2, r0, m1), 'b'test/qos/6510301014/temperature'', ... (5 bytes)
[15:32:17] PUBLISH REQUESTED | QoS=2 | Message='Hello' | msgid=1
Enter message to publish: [15:32:17] DEBUG | Received PUBREC (Mid: 1)
[15:32:17] DEBUG | Sending PUBREL (Mid: 1)
[15:32:17] DEBUG | Received PUBCOMP (Mid: 1)
[15:32:17] PUBLISHED | msgid=1
```

## Subscriber_qos.py Output

```
c:\Users\FDT-CDTI\Documents\IOT\Iot-class-2025-gateway\app\subscriber_qos.py:25: DeprecationWarning: Callback API version 1 is deprecated, update to latest version
  client = mqtt.Client()
[15:33:26] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
[15:33:26] DEBUG | Received CONNACK (0, 0)
[15:33:26] Connected with result code 0
[15:33:26] DEBUG | Sending SUBSCRIBE (d0, m1) [(b'test/qos/6510301014', 2)]
[15:33:26] DEBUG | Received SUBACK
```