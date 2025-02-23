maqueen.writeLED(maqueen.LED.LEDLeft, maqueen.LEDswitch.turnOn) basic.showLeds(` # # # # # # # . # # # # # # # # # # . # # # . # # `) maqueen.motorStop(maqueen.Motors.All) IR.IR_init() Maqueen_V5.I2CInit() bluetooth.startLEDService() let strip = neopixel.create(DigitalPin.P0, 24, NeoPixelMode.RGB) minode.FanControl_1(AnalogConnName.Analog_A2, 12) datalogger.log(datalogger.createCV("100", 100)) keyboard.startKeyboardService() mouse.startMouseService() media.startMediaService() absmouse.startAbsoluteMouseService() gamepad.send( gamepad._buttons(GameButton.none, true), 191, 192, gamepad._dpad(GameDirection.noDirection), 192, 192 ) RTC_DS1307.DateTime( 2019, 1, 17, 12, 31, 19 ) ESP8266_IoT.initWIFI(SerialPin.P8, SerialPin.P12, BaudRate.BaudRate115200) ESP8266_IoT.setData( "Thehan12345678908282392939393387gyguyvuyygygg67byt4v7y4tb7ybv7b4t7yv4t", 100 ) ESP8266_IoT.connectSmartiot("", "") ESP8266_IoT.setMQTT( ESP8266_IoT.SchemeList.TCP, "192.168.70.107", "Thehan ", "192.168.70.107", "192.168.70.107" ) ESP8266_IoT.setIFTTT("Thehan6636465664", "192.168.70.107") let _4digit = sonar.ping( DigitalPin.P9, DigitalPin.P9, PingUnit.Inches ) tft24.backlightCtrl(tft24.BlkCmdEnum.BlkOpen) OLED.init(128, 64) record.setMicGain(record.AudioLevels.Medium) minode.FanControl_1(AnalogConnName.Analog_A1, 12) servos.P0.setAngle(90) turtle.turnLeft() basic.forever(function () { })usb code
main.py
def on_sensor_error(errorMessage, errorCode, port):
    global strip
    strip = 1
    smarthome.led_brightness(AnalogPin.P0, True, 30)
dstemp.sensor_error(on_sensor_error)

def on_received_number(receivedNumber):
    OLED.init(receivedNumber, receivedNumber)
radio.on_received_number(on_received_number)

strip = 0
IP_address = 0
music.play(music.string_playable("C5 B A G F E D C ", 120),
    music.PlaybackMode.IN_BACKGROUND)
music.play(music.string_playable("C D E F G A B C5 ", dstemp.celsius(DigitalPin.P16)),
    music.PlaybackMode.IN_BACKGROUND)
create_message_error_message_port = IP_address
IP_address = create_message_error_message_port
IP_address += sonar.ping(DigitalPin.P1, DigitalPin.P16, PingUnit.INCHES)
smarthome.crash_sensor_setup(DigitalPin.P0)
smarthome.crash_sensor_setup(DigitalPin.P1)
WiFiBit.execute_http_method(HttpMethod.GET, "google.com", 80, "/search?q=something")
smarthome.crash_sensor_setup(DigitalPin.P16)
OLED.init(128, 64)
WiFiBit.write_blynk_pin_value("510", "A0", "14dabda3551b4dd5ab46464af582f7d2")
WiFiBit.write_blynk_io_tpin_value("1", "V1", "BzMEzpZ9Bud9ZUXZoJVEkbfneCavDVDx")
WiFiBit.connect_to_wi_fi_network("SSID", "key")
WiFiBit.execute_at_command("AT", 1000)
WiFiBit.connect_to_wi_fi_bit()
basic.show_arrow(ArrowNames.NORTH)

def on_forever():
    smarthome.motor_fan(AnalogPin.P16, True, 10)
basic.forever(on_forever)
Extensions
radio, *
microphone, *
microbit-dstemp, github:bsiever/microbit-dstemp#v0.1.26
pxt-sonar, github:microsoft/pxt-sonar#v0.0.6
smarthome-kit, github:tinkertanker/pxt-smarthome#v2.2.2
pxt-wifi, github:solderedelectronics/pxt-wifi#v1.1.0
usb code
dstemp.sensorError(function on_sensor_error(errorMessage: string, errorCode: number, port: number) {

    strip = 1
    smarthome.ledBrightness(AnalogPin.P0, true, 30)
})
radio.onReceivedNumber(function on_received_number(receivedNumber: number) {
    OLED.init(receivedNumber, receivedNumber)
})
let strip = 0
let IP_address = 0
music.play(music.stringPlayable("C5 B A G F E D C ", 120), music.PlaybackMode.InBackground)
music.play(music.stringPlayable("C D E F G A B C5 ", dstemp.celsius(DigitalPin.P16)), music.PlaybackMode.InBackground)
let create_message_error_message_port = IP_address
IP_address = create_message_error_message_port
IP_address += sonar.ping(DigitalPin.P1, DigitalPin.P16, PingUnit.Inches)
smarthome.crashSensorSetup(DigitalPin.P0)
smarthome.crashSensorSetup(DigitalPin.P1)
WiFiBit.executeHttpMethod(HttpMethod.GET, "google.com", 80, "/search?q=something")
smarthome.crashSensorSetup(DigitalPin.P16)
OLED.init(128, 64)
WiFiBit.writeBlynkPinValue("510", "A0", "14dabda3551b4dd5ab46464af582f7d2")
WiFiBit.writeBlynkIoTPinValue("1", "V1", "BzMEzpZ9Bud9ZUXZoJVEkbfneCavDVDx")
WiFiBit.connectToWiFiNetwork("SSID", "key")
WiFiBit.executeAtCommand("AT", 1000)
WiFiBit.connectToWiFiBit()
basic.showArrow(ArrowNames.North)
basic.forever(function on_forever() {
    smarthome.motorFan(AnalogPin.P16, true, 10)
})
Extensions
radio, *
microphone, *
microbit-dstemp, github:bsiever/microbit-dstemp#v0.1.26
pxt-sonar, github:microsoft/pxt-sonar#v0.0.6
smarthome-kit, github:tinkertanker/pxt-smarthome#v2.2.2
pxt-wifi, github:solderedelectronics/pxt-wifi#v1.1.0

