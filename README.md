# Wearable Sleep Monitoring IoT Device

## Introduction
Sleep deprivation has been linked to impairments in cognitive functioning, decision-making, and reaction times. The cumulative effects of sleep deprivation can be alarming, making it important to devise measures to monitor and improve sleep quality.

The goal of this project is to build a device that can be worn around the wrist during sleep to analyze the sleeping pattern and depth of sleep using various sensors. The device includes an MPU 6050 gyroscope and accelerometer to detect sudden movements and determine the sleeping position in bed, as well as a pulse sensor to analyze stress levels during sleep. The data from these sensors is analyzed in real-time using the PLX-DAQ feature to provide a comprehensive analysis of the wearer's sleep.

## Components
* Arduino UNO
* MPU6050 Gyroscope + Accelerometer
* Pulse sensor
* Bluetooth module

## Logic and Working
The Euler values from the gyroscope are used to identify the sleeping position of the subject. These values are also used to measure sudden movements during sleep. Whenever consecutive fluctuations in the gyroscopic output are detected, the program considers it as an interference in sleep. A variable called "Sleep Points" is assigned to track the quality of sleep, starting at 1000 every time the device is activated. Every time an interference is detected, the Sleep Points value is decremented.

The device is also capable of indicating the wearer's stress level during sleep by analyzing the heartbeats per minute (BPM) data from the pulse sensor. Interruptions during sleep, such as sudden movements or changes in sleeping position, can also be detected using the combination of gyroscope and pulse sensor data.

## Conclusion

This project has been an innovative experience that demonstrates the potential for simple circuits to have various applications in daily life. The device has the potential to be implemented in military settings and can be modified for future start-up opportunities. Working with the 555 Timer IC and the BC547 transistor provided valuable insights into their working principles. However, the device does have some limitations, such as an inability to detect motion out of its line-of-sight or from more than 2 meters away. Despite these limitations, the project has a vast scope for modifications to the design and we are proud of its potential for improving sleep quality.
