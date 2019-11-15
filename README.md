# arduino
Arduino experimental

1 Arduino Nano as UART adapter, any sketch will be ignored.
atmega 326, 16Ghz
nano 5v -> pro mini 5v

+5v -> VCC  
GRD -> GRD  
TX -> TX  
RX -> RX  
short GND+RESET on NANO on ISCP  

IDE:  
Board: Pro Mini  
Programmer: "AVRISP mkII"  

=============================

2 Arduino Nano as ISP  
Arduino ISP sketch installed to NANO  

nano 5v -> pro mini 5v

+5v -> Vcc  
GND -> GND  
D10 -> RST  
D11 -> D11  
D12 -> D12  
D13 -> D13  
4,7uF Capacitor on RST+GND (not worked for me if skip)

IDE:  
Board: Pro Mini  
Programmer: "Arduino as ISP"  
menu Sketch->Upload using programmer  

=============================

3 Using 3rd party USB-TTL USB-STC-ISP | PL2303 USB to Serial  
Adapter -> pro mini 5v  
+5v -> Vcc  
GRD -> GRD  
TX -> TX  
RX -> RX  
RESET ->GRN (!!Not GND!!) - this could be not soldered, so it possible to use 2 pin on PL2303 instead, solder carefully.

if RESET connected DO NOT press "reset" on Pro Mini on uploading, it will BURN PL2303  
if no RESET pin - need press "reset" on Pro Mini when uploading sketch, right before "uploading.." message in IDE

4 Using MX-USBISP-v3.0 as USBasp  
Hack it to use as USBAsp  
still in progress, no luck yet  


