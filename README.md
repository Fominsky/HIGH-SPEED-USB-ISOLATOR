# High-speed USB isolator based on ADuM3165/ADuM3166

When connecting a USB device to a PC or laptop, there is a risk that the device may be faulty or may fail during operation. This is especially relevant during the development and debugging of devices that connects to your PC.

Connecting a malfunctioning USB device can easily lead to the failure of the USB hub in your PC, and in the case of laptops, the hub is often located on the same substrate as the processor. Thus, there is a risk that if something goes wrong, you will have to replace the processor in your laptop.

A USB isolator will protect your PC from USB-related issues. In the worst-case scenario, the ADuM3165/6 chip itself may fail, but your PC should be fine.

## Description
The device has 3 USB ports: Host USB, External Power USB, and Device USB.
Host USB is connected to your computer, Device USB is connected to your device that needs to be isolated, and External Power USB is connected to an external power source for powering the device connected to the Device USB port.

The device has its own low-power galvanically isolated DC-DC converter. The DC-DC converter also has converter overload protection. Therefore, the device can be used without external power for communication with low-power devices or devices that have their own power source.

The maximum current of the DC-DC converter is 200 mA. If this value is exceeded, the load is disconnected, and the "Overload" red LED lights up. The load will be disconnected either until the protection is reset by pressing SW1 button (Reset_Button) or until the USB is disconnected from the host USB and reconnected. 

To connect more powerful loads, you can use the External Power USB port. It is important to note that this USB is not isolated from the Device USB but is not electrically connected to the Host USB. A good solution would be to connect a power adapter from a mobile device to the external power USB.

When external power is connected, the built-in DC-DC converter is disabled. Note: as I mentioned before, the overload protection only works with the built-in DC-DC converter, so the overload protection is also disabled.

##

This Repository contains Gerber files, BOM, and step model. All you need to make an isolator. 

![image](https://github.com/Fominsky/HIGH-SPEED-USB-ISOLATOR/assets/15094757/9cb8d0ad-a32b-41e1-ab38-f9632be99db0)

![image](https://github.com/Fominsky/HIGH-SPEED-USB-ISOLATOR/assets/15094757/82485f93-f85f-4e32-8115-b1f6119b4b3d)


