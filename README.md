# Healthy Battery Charging

## About

Forked from: https://github.com/vbresan/HealthyBatteryCharging

Make your smartphone or tablet battery last longer!

Good range to aim for when charging a Li-ion battery is from about 40 to 80 percent in one go. A bunch of tiny charges throughout the day is your second best bet, and going from zero to 100 and then 100 to zero on a regular basis will put the most strain on your lithium-ion battery.

The goal with battery_zigbee is to build off of the good work by vbresan with Healthy Battery Charger and extend beyond a notification into action.
With a properly configured home network with home assistant OS running on a mini PC with a Zigbee stick, you can configure a basic zigbee plug like this: https://www.amazon.com/SONOFF-Zigbee-SmartThings-Amazon-Needed/dp/B08Y87WD1X
To be switched on or off using the Home Assistant OS, using the home assistant OS app or by accessing it via the website. The goal with this project is to combine that properly configured home assistant OS with the notification code to switch off the charger if the charger is plugged in and battery > 80%. After 1 hour has passed, you can switch the plug back on and continue monitoring for 80%. Time can be adjusted again as required. Maybe even synchronized to alarms?

#TODO:
     Add the documentation/FSM diagram that would best describe states for the app
     Also make the app duh.


The app itself is optimized for low battery consumption, running in the background and checking the battery level every 15 minutes. The exact timing of these checks depends on the Android OS, which might schedule them alongside other tasks or delay them when in sleep mode. As a result, the battery level may slightly exceed the high threshold while charging or drop slightly below the low threshold while discharging before you receive a notification.

For those who want to know more technical details about Li-ion batteries:  
http://batteryuniversity.com/learn/article/how_to_prolong_lithium_based_batteries
