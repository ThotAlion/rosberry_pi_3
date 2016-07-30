# rosberry_pi_3
This ROS package is to manage the GPIO of the Raspberry Pi 3 and the internal parameters. I decided to make a specific package for the Raspberry Pi 3 of the drone I use because a generalisation could be too much time consuming, and the programming task here is not awful thanks to the Raspberry community, there is much documentation on how to manage GPIO.
It can also be useful to have RAM memory, CPU load and CPU temperature to indentify future bugs.
There is no specific message definition in this package.

## What is published
- /cpu_temperature : Float32 giving the temperature of the CPU in Celsuis (sampling period : 10s)
- /cpu-load : Int8 giving the CPU load in percentage (sampling period : 10s)
- /ram_load : Int8 giving the RAM load in percentage (sampling period : 10s)

## Which to subscribe ?
- /pan : Int16 to provide. From 0 to 1000 (from end to end) plugged on GPIO number X
- /tilt : Int16 to provide. From 0 to 1000 (from end to end) plugged on GPIO number X
- /LED_acq : Bool equal to true if the drone sees and follow a tag
- /LED_cam_on : Bool equal to true when the camera flow is operating
- ...

## Services ?
No services for the moment

## Serial port
Notice the serial port is not taken by this package to divide the code.
