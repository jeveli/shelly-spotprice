 
# Add Nordpool price 💶 switching to your shelly Plus 1 PM device
 
This code works if you live in Estonia 🇪🇪, Lithuania 🇱🇻, Latvia 🇱🇹 or Finland 🇫🇮. Just change the country code in the API endpoint.

# Script setup
Make sure your Shelly device is connected to the Internet and accessible from LAN.
* Login to the cloud ☁️
* Find device
* ![image](https://user-images.githubusercontent.com/7755806/203836506-48ee1dd3-49dc-4262-a608-3fc9b090dd90.png)

* Click settings
![image](https://user-images.githubusercontent.com/7755806/203836573-d62411d9-f7f4-453b-85c2-e163a4c0fc34.png)


* Firmware Versions
![image](https://user-images.githubusercontent.com/7755806/203836755-47bc89d3-2e3c-445e-9e67-9f4c6649ca57.png)


* Update the firmware
![image](https://user-images.githubusercontent.com/7755806/203836803-b2604006-a9bc-4917-9f43-a353f551965d.png)


* Device information
![image](https://user-images.githubusercontent.com/7755806/203836851-71542fc1-c9c5-41f3-91ad-8c9556fa8d26.png)


* Device IP
This should open in a new browser window with local access to Shelly's device.
![image](https://user-images.githubusercontent.com/7755806/203836905-7268bda2-faae-4927-b62e-2feba05750e4.png)

 
## Installing Script
 

* Click on **Devices** button
* Click on **Debug** button
* Enable **Mqtt debug:** and **Websocket debug::**
* Click on **Scripts** button
* Open **Add Script**
* Enter **script name**
* Open script  `https://github.com/jeveli/shelly-spotprice/commit/227bfad28490e51ed9c9c53f5b92d91b29792a1b`
* Copy the script and paste it into the editor
* Click on **Save and run**
 

## Configure API endpoint
Find `api_endpoint` and change `#COUNTRY_CODE#` 🌍 to ee, lv, lt or fi
```
api_endpoint: "https://dashboard.elering.ee/api/nps/price/fi/current"
```
 
## Set your price point  👈
Find configuration value `price_limit` will be set when your device turns on or off. Prices don’t include VAT and are measured in EUR/MWh
### Example
```  price_limit: 400 ```
Will set toggling threshold for the device to 400 EUR/MWh
