# Bluetooth-bike-tire-pressure-sensor
Bluetooth tire pressure sensor project. Measures pressure, tempreture and battery percentage.  Readings could be displayed with TPMSII android app from Play Store. Sensor is designed to be integrated with a valve and to bemounted inside a bike rim. 

This project was developed around nrf52832 microcontroller with Segger Embedded Studio and Nordic Semi SDK statement v17.1.0. Softdevice v7.2.0 (Bluetooth stack) from Nordic Semi was used.

For this project a custom PCB was designed in Altium Designer and a custom housing in TinkerCAD.

Functional description:
The sensor broadcasts pressure, temperature and battery data over BLE. The data format is compatible with the one used by BLE pressure sensor from aliexpress, like these:
https://youtu.be/v4x5Eum56oU

TPMSII Android app maps sensors using an ID coded in each sensor name and advertising data. Data format used by orginal sensors is described here:
https://github.com/ra6070/BLE-TPMS

My sensor is motion activated. It advertises data as long as the motion is detected. When motion stops for longer than 2 minutes, sensor stops advertising to preserve a battery. 

The sensor is powered using two CR927 batteries. The estimated battery lifetime is 3 years minimum assuming daily usage of 15 minutes.

Photo gallery:
![20230104_091022](https://user-images.githubusercontent.com/72305802/226428673-33b45659-67bd-4498-91b1-5f71a9df69f5.jpg)
![20230301_073012](https://user-images.githubusercontent.com/72305802/226428676-61e56e1b-3252-44d9-a43e-24c11e202a98.jpg)
![20230305_143638](https://user-images.githubusercontent.com/72305802/226428685-80dd24d9-09ad-409f-8d01-21f51a7d8179.jpg)
![20221223_105532](https://user-images.githubusercontent.com/72305802/226428690-2f23b92e-b379-42d3-8c4d-dfb233cb2ac4.jpg)
![20221223_105542](https://user-images.githubusercontent.com/72305802/226428702-3d266636-2c56-4635-9112-ff2b203d5249.jpg)
![20221226_151808](https://user-images.githubusercontent.com/72305802/226428730-d8d34971-0b07-4f8d-97da-a6da8e5bbca5.jpg)
![20221229_220139](https://user-images.githubusercontent.com/72305802/226428737-43b9b0ae-7e74-42c2-ac34-f868834cfe67.jpg)
![20221229_221225](https://user-images.githubusercontent.com/72305802/226428744-faffe661-5c83-409f-84b3-b9592b63da46.jpg)
![image](https://user-images.githubusercontent.com/72305802/226429002-f6b9270b-e25a-49b4-b54c-5680b532b8f7.png)
