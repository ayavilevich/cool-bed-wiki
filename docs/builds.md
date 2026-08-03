## Simple build

A simple build will cool one pad.

![Diagram](img/two-buckets-diagram.png)

Follow [getting started](getting-started.md) for more details.

## Flow monitoring build

If you add a [flow sensor](components/flow-sensor.md) to the circulation loop of the simple system, then you can get feedback on the operation of the pump. This is useful if you want to drive the pump at variable speeds.
Not recommended unless you are looking to experiment with new modes of operation.

You can optionally add a temperature sensor on the returning water pipe for even more telemetry.

## Current monitoring build

If you can build or get a [controller board](components/controller-board.md) with current measurement capabilities then you can configure the firmware to detect and stop on current that is either too high or too low. This can help identify stalls, air blocks, no water condition, etc.
The firmware currently supports INA226 ICs and each output can have such an IC measuring it.

## Double bed build

If you want to create a system for two people you must take one of two approaches. One, if you just want to cool both people in a double bed to the same temperature. Another, if you want individual control over the temperature at each side.

### Simpler, same temperature control

Either rotate the [pad](components/mattress-pad.md) 90 degrees to share it or get a larger pad (there are single and double options at the online stores).
You might need to get a stronger [circulation pump](components/pumps.md) if your pad is larger.
You can also put two single pads in series but one might end up being colder than the other.

### Separate temperature control

You need to build two separate systems with twice the pumps, loops, controllers, etc. The one thing that you can share is the cold container.
So you end up with 3 containers, one for the left side, one for the right side and a shared one for cold water storage.

When you configure your first controller, you can give it a non default hostname and MQTT root topic. Once you do, you can have another controller on the same WiFi and HA without conflicts. You can have as many controllers as your WiFi network will handle.
