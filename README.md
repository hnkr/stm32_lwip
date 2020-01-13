# Running LwIP TCP/IP Stack on STM32 Microcontroller
- Microcontroller: STM32F767
- Development Board: Nucleo-144

## Requirements
- STM32CubeIDE
- lwIP TCP/IP Stack
- tcpdump to capture network

## Build & Flash & Run
- Build:
    -  Regular build project via STM32CubeIDE
- Flash & Run:
    - Flash into microcontroller via STM32CubeIDE (via stlink or jlink)
    - Run via reset button of the board or debug interface of STM32CubeIDE

## Projects
- lwip_203
    - Project generated via STM32CubeIDE and its configurator (cubeMX)
    - FreeRTOS based
    - When DHCP Server assigns an IP Address to the board then you can test communication via ping / ICMP.
- lwip_212
    - lwip sources of lwip_203 is updated with the latest version lwip of now, 2.1.2.
    - All functionalities are the same as lwip_203's.

## Working Principle
When it starts running, LD3 RED Led will start blinking<br />
DHCP Client will be started so, DHCP Discovery packets should be seen on your network.


## Testing

- You should see DHCP discovery messages via tcpdump (with -vv flag and port / protocol filter) or dhcp dump:<br />
- You should have response for your ping.




