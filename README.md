# esphomeprojects
A collection of various esphome projects.

**Lilygo / TTGO T5 v2.2 2.9" Board**

See [epaper29.yaml](https://github.com/cvocvo/esphomeprojects/blob/main/epaper29.yaml) for more details. Has some power saving optimizations / deep sleep configurations for:
- Mon-Friday 8am - 4pm check -- sleep the device during this time. This probably needs to be a bit better for a dynamic sleep time if it wakes up in the middle.
- Daily 10pm - 6am sleep
- 5:50am check -- The overnight sleep usually has some level of time drift. Maybe my RTC pin is wrong or something. This allows for 10min of drift when it wakes up so it doesn't sleep for an extra 8 hours.
![t5-2 9in-yamlv33](https://user-images.githubusercontent.com/355711/184048069-e3dd4af2-92b8-4ac9-b54d-7c409302a02a.jpg)
