# esphomeprojects
A collection of various esphome projects.

## Lilygo / TTGO T5 v2.2 2.9" Board
**Board Info**
- Board: https://www.aliexpress.com/item/2251832664072244.html
- Schematic: https://github.com/Xinyuan-LilyGO/LilyGo-T5-Epaper-Series/blob/master/schematic/T5V2.2.pdf

**Power Optimizations**

See [epaper29.yaml](https://github.com/cvocvo/esphomeprojects/blob/main/epaper29.yaml) for more details. Has some power saving optimizations / deep sleep configurations for:
- Mon-Friday 8am - 4pm check -- sleep the device during this time. This probably needs to be a bit better for a dynamic sleep time if it wakes up in the middle.
- Daily 10pm - 6am sleep
- 5:50am check -- The overnight sleep usually has some level of time drift. Maybe my RTC pin is wrong or something. This allows for 10min of drift when it wakes up so it doesn't sleep for an extra 8 hours.
- Running the wifi in aggressive power saving mode

**Battery Info:**
- Using this battery: [3.7V 3500 mAh Polymer Li Battery 706062 PH1.25](https://www.ebay.com/itm/175271912281)
- **NOTE:** Make sure you get the connector option: 706062 2pin 1.25**F**
  - If you don't get the "F" variant the positive and negative terminals will be swapped and won't match the v2.2 2.9" board terminals.
- Specs from the manufacturer:
  - Built-in protection circuit PCM for prevent over charging or over discharging.
  - Full Charge: 4.1V 
  - Discharges Down To: 3.0V (the li battery will not work when less than 3.0v)

![t5-2 9in-yamlv33](https://user-images.githubusercontent.com/355711/184048069-e3dd4af2-92b8-4ac9-b54d-7c409302a02a.jpg)
