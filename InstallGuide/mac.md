Installation instructions for Mac OS
=====================================

- Install latest Arduino IDE from [arduino.cc](https://www.arduino.cc/en/Main/Software)
- Open Terminal and execute the following command (copy->paste and hit enter one by one):

  ```bash
  mkdir -p ~/Documents/Arduino/hardware
  cd ~/Documents/Arduino/hardware
  git clone https://github.com/Heltec-Aaron-Lee/WiFi_Kit_series.git heltec
  cd heltec/esp32
  git submodule update --init --recursive
  cd tools
  python get.py
  cd ~/Documents/Arduino/hardware/heltec/esp8266
  git submodule update --init --recursive
  cd tools
  python get.py
  ```
- If you get errors in "python get.py" with "http_error", just try that command again;
- If you get the error below. Install the command line dev tools with xcode-select --install and try the command above again:
  
```xcrun: error: invalid active developer path (/Library/Developer/CommandLineTools), missing xcrun at: /Library/Developer/CommandLineTools/usr/bin/xcrun```

```xcode-select --install```

- Restart Arduino IDE

