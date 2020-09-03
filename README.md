# Dahua VTO Doorbell integration into Home Assistant
Integrate a Dahua VTO doorbell into Home Assistant. The instructions are made for a manual Home Assistant installation (without Docker) on a Raspberry Pi 4. 
# Credits
Credits goes to @riogrande75 who wrote that complicated integration Original code can be found in @riogrande75/Dahua
# Before you begin
Make some modifications to your Dahua VTO doorbell
1. Enable Motion detection (if you want to listen to video detection events)
2. Enable the SIP Server. You can specify the same IP address as your doorbell. Only with this option available you the script will listen to events when you press the caller button
# Further useful information:
Dahua event API documentation is part of the repository
New firmware can be found here: https://www.dahuasecurity.com/support/downloadCenter/firmware?child=607

# Steps
1. Create and run a service for the event listener script
2. Modify the event listener script from @riogrande75 to publish events to a MQTT broker on events and save screenshots to your folder of choice
3. create the necassary sensors in Home Assistant
4. create the necassary automation(s) in Home Assistant to send you a decent notification when someone presses the your doorbell
