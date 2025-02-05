## Arduino STM32(2024/09/04 commit245b97a)の修正バージョン

- オリジナルへの修正 Adafruit_ILI9341_STM、Adafruit_SSD1306の不具合対応  
- platform.txtの修正:compiler.path={runtime.tools.arm-none-eabi-gcc-4.8.3-2014q1.path}/bin/  
- jssc.jar の差し替え(jssc-2.9.6.jar)  
- platform.local.txtの追加  

以下原文
=======


Arduino STM32
=============

## Notice
This software is experimental and a work in progress.
Under no circumstances should these files be used in relation to any critical system(s).
Use of these files is at your own risk.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Summary:
This repo contains the "Hardware" files to support STM32 based boards on Arduino version 1.8.x (some older versions may also work) including [LeafLabs Maple, and Maple mini](http://www.leaflabs.com/about-maple/), and other generic STM32F103 boards.

## Background & Support:
* Based on https://github.com/bobc/maple-asp, which is in turn based on LibMaple by Leaflabs
* **Please read the wiki (https://github.com/rogerclarkmelbourne/Arduino_STM32/wiki) for full details**
* See also my blog: http://www.rogerclark.net/stm32f103-and-maple-maple-mini-with-arduino-1-5-x-ide/
* **NEW: Main support site for using STM32 boards with the Arduino IDE: http://www.stm32duino.com/**
* Original LeafLabs "Docs:" http://docs.leaflabs.com/docs.leaflabs.com/index.html

## Known issues
* Use of static variables inside functions greatly increase the code size becuase additional code is needed for thread-safe handling of these statics.
If this is a problem for your application, please edit platform.txt and add -fno-threadsafe-statics the compiler.cpp.flags 


## Additional Links & Info:
* https://www.hackster.io/rayburne/4-dollar-90-mips-32-bit-72-mhz-arm-arduino

## Purchase info:
### Entry level boards
* [Ebay search for "arduino maple"](http://www.ebay.com/sch/i.html?_from=R40&_sacat=0&LH_BIN=1&_nkw=arduino+maple&_sop=15) (currently costs <$5 with shipping)
* [AliExpress search for "leaflabs maple"](http://www.aliexpress.com/wholesale?catId=0&initiative_id=SB_20150607085526&SearchText=leaflabs+maple)

### Bigger boards (You need to load the stm32duino bootloader)
Some suppliers have this board e.g.
* [ STM32F103VET ](http://www.ebay.com.au/itm/1PCS-STM32F103VET6-ARM-STM32-Minimum-System-Development-Board-Arduino-M77-/301433302819)
* [There is also a STM32F103ZET board which also works, however they are not always available. They have been listed as "STM32F103ZET6 Minimum System Development Board ARM STM32 Cortex-m3 M75"](http://www.ebay.com.au/itm/1pcs-STM32F103ZET6-Minimum-System-Development-Board-ARM-STM32-Cortex-m3-M75-/291305557264)
