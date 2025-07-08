# AI gesture sensor control system

## Example

Initialize the gesture sensor.

``` block
grove.initGesture()
basic.forever(function () {
	
})


```

## Example

Add on Gesture for up and down.
    
``` block
grove.onGesture(GroveGesture.Up, function () {
    
})
grove.onGesture(GroveGesture.Down, function () {
    
})
```

## Example

Turn on the light.

``` block

basic.forever(function () {
	pins.analogWritePin(AnalogPin.P2, 1023)
})
```

## Check Point 1

Now try to control the light using gesture. 
Set up to turn on the light and down to turn off the light.

``` block
grove.initGesture()
basic.forever(function () {
	
})


grove.onGesture(GroveGesture.Up, function () {
    pins.analogWritePin(AnalogPin.P2, 1023)
})
grove.onGesture(GroveGesture.Down, function () {
    pins.analogWritePin(AnalogPin.P2, 0)
})
```

## Example

Add on Gesture for forward and backward.

``` block
grove.onGesture(GroveGesture.Forward, function () {
    
})
grove.onGesture(GroveGesture.Backward, function () {
    
})
```

## Example

Turn on the ac.

``` block

basic.forever(function () {
	pksdriver.MotorRun(pksdriver.Motors.M1, pksdriver.Dir.CW, 70)
})
```

## Check Point 2
Now try to control the motor of ac using gesture. 
Set forward to turn on the ac and backward to turn off the ac

``` block
grove.initGesture()
basic.forever(function () {
	
})


grove.onGesture(GroveGesture.Forward, function () {
    pksdriver.MotorRun(pksdriver.Motors.M1, pksdriver.Dir.CW, 70)
})
grove.onGesture(GroveGesture.Backward, function () {
    pksdriver.MotorRun(pksdriver.Motors.M1, pksdriver.Dir.CW, 0)
})
```


## Example

Add on Gesture for left and right.

``` block
grove.onGesture(GroveGesture.Left function () {
    
})
grove.onGesture(GroveGesture.Right, function () {
    
})
```

## Example

Open the door.

``` block

basic.forever(function () {
	pksdriver.servo(pksdriver.Servos.S1, 90)
})
```

## Check Point 3
Now try to control the door using gesture. 
Set left to open the door and right to turn close the door


``` block
grove.initGesture()
basic.forever(function () {
	
})
grove.onGesture(GroveGesture.Left, function () {
    pksdriver.servo(pksdriver.Servos.S1, 90)
})
grove.onGesture(GroveGesture.Right, function () {
    pksdriver.servo(pksdriver.Servos.S1, 0)
})
```
## Assessment 1
Control the light, ac and door. Your task is to create a micro:bit-controlled smart room that will use gesture to 
turn on or off  the light, turn on or off the ac and open and close the door.

``` block
grove.onGesture(GroveGesture.Down, function () {
    pins.analogWritePin(AnalogPin.P2, 0)
})

grove.onGesture(GroveGesture.Right, function () {
    pksdriver.servo(pksdriver.Servos.S1, 0)
})
grove.onGesture(GroveGesture.Backward, function () {
    pksdriver.MotorRun(pksdriver.Motors.M1, pksdriver.Dir.CW, 0)
})
grove.onGesture(GroveGesture.Up, function () {
    pins.analogWritePin(AnalogPin.P2, 1023)
})
grove.onGesture(GroveGesture.Forward, function () {
    pksdriver.MotorRun(pksdriver.Motors.M1, pksdriver.Dir.CW, 70)
})
grove.onGesture(GroveGesture.Left, function () {
    pksdriver.servo(pksdriver.Servos.S1, 90)
})
grove.initGesture()
basic.forever(function () {
	
})
```

## Assessment 2

Make a comfortable environment for watching movie. Your task is to create a micro:bit-controlled smart room that makes a perfect environment for watching move. 
Control the light to be dimmer but does not go off, turn on the ac and close the door. 
Use the gesture 'Wave'.

``` block
grove.onGesture(GroveGesture.Down, function () {
    pins.analogWritePin(AnalogPin.P2, 0)
})
grove.onGesture(GroveGesture.Wave, function () {
    pins.analogWritePin(AnalogPin.P2, 200)
    pksdriver.MotorRun(pksdriver.Motors.M1, pksdriver.Dir.CW, 70)
    pksdriver.servo(pksdriver.Servos.S1, 0)
})
grove.onGesture(GroveGesture.Right, function () {
    pksdriver.servo(pksdriver.Servos.S1, 0)
})
grove.onGesture(GroveGesture.Backward, function () {
    pksdriver.MotorRun(pksdriver.Motors.M1, pksdriver.Dir.CW, 0)
})
grove.onGesture(GroveGesture.Up, function () {
    pins.analogWritePin(AnalogPin.P2, 1023)
})
grove.onGesture(GroveGesture.Forward, function () {
    pksdriver.MotorRun(pksdriver.Motors.M1, pksdriver.Dir.CW, 70)
})
grove.onGesture(GroveGesture.Left, function () {
    pksdriver.servo(pksdriver.Servos.S1, 90)
})
grove.initGesture()
basic.forever(function () {
	
})

```

<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
