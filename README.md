adxl345-python3
==============

adx library for python3.  It is based on the [python2 library](https://github.com/pimoroni/adxl345-python)

You must have smbus for python3 installed. [Get it from here](https://github.com/cloudformdesign/adxl345-python3)

Raspberry Pi Python i2c library for the ADXL3453-axis MEMS accelerometer IC which is used in breakout boards like the Adafruit ADXL345 Triple-Axis Accelerometer (http://shop.pimoroni.com/products/adafruit-triple-axis-accelerometer).

This library is a basic implementation of the i2c protocol for the IC offering a simple way to get started with it on the Raspberry Pi.

You can import the module and get a sensor reading like this:

    from adxl345 import ADXL345

    adxl345 = ADXL345()

    axes = adxl345.getAxes(True)
    print "ADXL345 on address 0x%x:" % (adxl345.address)
    print "   x = %.3fG" % ( axes['x'] )
    print "   y = %.3fG" % ( axes['y'] )
    print "   z = %.3fG" % ( axes['z'] )

or you can run it directly from the command line like this:

    sudo python ADXL345.py
    
which will output the current x, y, and z axis readings in Gs.
