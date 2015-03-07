# openHAB CAN bus bundle
Here I plan to develop a set of bundles that provide Java access to system level CAN bus drivers in the openHAB framework. The aim is to separate the CANopen protocol implemtentation in my [CANopen binding](https://github.com/jgeisler0303/openHAB_CANopen_Binding) from the actual details of accessing the bus.

# Currently
Currently the bundle only provides the https://github.com/entropia/libsocket-can-java library to interested bundles in openHAB. The version in this repo only contains the native files for x86 linux machines because I don't know how to make multi-architecture JNI libraries. But I could make a different branch for an RPi version.

# Future Plans
I plan to provide a unified way for accessing at least
* [socketcan](http://en.wikipedia.org/wiki/SocketCAN), used e.g. for the popular Raspberry Pi CAN bus shields like e.g. [this](http://skpang.co.uk/catalog/pican-canbus-board-for-raspberry-pi-p-1196.html) or [my cloned version](https://github.com/jgeisler0303/AGCON/tree/master/Hardware/RPiShield) of it.
* [can4linux](http://en.wikipedia.org/wiki/Can4linux), used e.g. for accessing the built-in can bus interface of the Banana Pi
* [slcan](https://gitorious.org/linux-can/can-misc/raw/282ad012d3418ca654211e7f212de7e2d86a56ea:slcan/SLCAN-API.pdf), a protocol for accessing a can bus via a serial (USB) connection. This is a very easy method if you have an Arduino and an [MCP2515](http://www.microchip.com/wwwproducts/devices.aspx?dDocName=en010406) to spare (sketch not written yet but should be straight forward, MCP2515 Arduino libraries already exist).
 
