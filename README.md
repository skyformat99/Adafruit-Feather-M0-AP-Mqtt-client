# Adafruit-Feather-M0-AP-Mqtt-client
Implementation of Mqtt client and SoftAP web server to change setting

# Maintain Connection to Broker
Manage the connection to the broker at all times and automatically attempt to reconnect to a Broker if the
Feather becomes disconnected for any reason.

# Embedded Web Server
    1. Create an embedded web interface for the Feather. The OLED will be used to display the IP address even
    if it is 169.x.x.x so someone can launch the web page using the IP.
    2. The web page should scan and list the available Wi-Fi networks (I saw some sample code for this also).
    3. Web page should allow the user to select an available SSID. It should have text fields to allow the user to
    type in connection info if required for the network they want to connect to. The web page should allow
    user to select connect to the network using DHCP and should provide the option to manual type in static
    IP address, subnet, and gateway.
    4. Web page should provide a textbox to type in the URL or IP of the MQTT Broker. There should be a
    connect button available to connect to the Broker. If a connection to the Broker is successful there
    should be a message that says it was successful on the web page.
    5. Web page should have a section to set the current date and time.
    6. All settings should be saved locally to the Feather. Once the Feather successfully connects to the Broker,
    all settings made on the Feather should also be published to the Broker via MQTT message so it can be
    stored there as well.
# Power management
    Manage the power consumption of the Feather as discussed here. The idea here is to preserve battery life when
    the Feather is running off the battery.
    https://learn.adafruit.com/adafruit-feather-m0-wifi-atwinc1500/power-management

# Additional Data
    Additional data should be sent from the Feather to the Broker. Along with ON or OFF status currently being sent,
    the Feather should also send the actual value of the analog reading. It should also send a timestamp. I am
    adding a real-time clock (RTC) to the Feather so this time should be used. I know you do not have the RTC so it
    will have to be tested on my side unless you choose to purchase one. Code can be written and commented out
    until it can be tested. Any other temporary method can be used to test the timestamp messaging functionality.
    A timestamp should also be sent along with the digital input data.
