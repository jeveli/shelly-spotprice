 
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

 
* Click on **Devices** button
![image](https://user-images.githubusercontent.com/7755806/203840748-ebfddbd4-154c-4ab4-85c2-509186f7627e.png)


* Click on **Debug** button, Enable **Mqtt debug:** and **Websocket debug**
![image](https://user-images.githubusercontent.com/7755806/203840793-38811213-aa09-41df-8700-d17215efe783.png)


* Click on **Debug** button, Enable **Mqtt debug:** and **Websocket debug**
![image](https://user-images.githubusercontent.com/7755806/203840914-16d16ab6-a3f6-4d73-977c-9a788999005f.png)



* Open **Add Script**
![image](https://user-images.githubusercontent.com/7755806/203840941-da0b549a-37f0-46c8-9a3d-0081177c4294.png)


* Enter **script name**
![image](https://user-images.githubusercontent.com/7755806/203841001-203a9b1b-c473-43d7-a74d-1f8992b2e966.png)


* Open script  `https://github.com/jeveli/shelly-spotprice/blob/58eee83dcfc41fec9947ae5b717a68cd90fb2f86/Finland%20Spot%20Price%20script`
![image](https://user-images.githubusercontent.com/7755806/203841254-18009801-bd18-4bb8-aa71-42d407df34cb.png)


* Copy the script and paste it into the editor and click on **Save and run**
![image](https://user-images.githubusercontent.com/7755806/203841322-be2f4df9-b34d-4037-998c-204766ff4476.png)


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
