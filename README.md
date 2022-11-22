# drop-pressure

Kafka stream will be used for real-time analytics purposes within the master work. 
The data source will be a pressure sensor, and an example of analysis will be an attempt to determine the moment of pressure drop. 
The work will also include the processing and transformation of that data, so working with streams.

In the paper, we will focus on the real-time capabilities of the Kafka system in relation to the available hardware architecture. 
Real data will be sampled, laboratory, sample rate will be 50 ms. We will be able to multiply that data.
We will have a producer who plays the role of a sensor, and we would provide the producer with finished data and he will read a 
large amount of data and send it at 50ms.

Using windowing and set it to for example to 10, 20 seconds and check the average value
we know that the standard value that should always be present is some x that we have defined in this case x is 10
if for that window the average value at any time
deviates by 2 percent from that x, then we say that there is an event in that range, and the event is drop of pressure
that would be the message that is send to the topic and another app would subscribe to the the topic, read the event and show it on a web page
