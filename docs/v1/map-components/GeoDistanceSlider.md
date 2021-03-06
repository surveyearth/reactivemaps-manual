{"bigh3": true}

## GeoDistanceSlider

![Image to be displayed](
https://i.imgur.com/FU4s0PQ.png)

A `GeoDistanceSlider` sensor component creates a location search based proximity slider UI widget. It is used for distance based filtering.

Example uses:

* finding restaurants in walking distance from your location.
* discovering things to do near a landmark.

### Usage

```js
<GeoDistanceSlider
  componentId="GeoDistanceSensor"
  appbaseField="location"
  title="Geo Distance Slider"
  unit="mi"
  range={
    {
      "start": 0,
      "end": 20
    }
  }
  defaultSelected={12}
  rangeLabels={
    {
      "start": "0 mi",
      "end": "20 mi"
    }
  }
  stepValue={1}
/>
```

### Props

- **componentId** `String`  
    unique id of the sensor, can be referenced in an actuator's `actuate` prop.
- **appbaseField** `String`  
    DB data field to be mapped with the component's UI view, used when a database query is made on this field.
- **title** `String` [optional]  
    title of the component to be shown in the UI.
- **unit** `String` [optional]  
    unit for distance measurement, uses `mi` (for miles) by default. Distance units can be specified from the following:  
    ![screenshot](https://i.imgur.com/STbeagk.png).
- **range** `Object`  
    an object with `start` and `end` keys and corresponding numeric values denoting the minimum and maximum possible slider values.
- **rangeLabels** `Object` [optional]  
    an object with `start` and `end` keys and corresponding `String` labels to show labels near the ends of the `GeoDistanceSlider` component.
- **defaultSelected** `Number` [optional]  
    pre-select a value from the range.
- **stepValue** `Number` [optional]  
    step value specifies the slider stepper. Value should be an integer between 1 and floor(#total-range/2). Defaults to 1.


### CSS Styles

All reactivebase and reactivemaps components are `rbc` namespaced.

![Annotated image]()

```html
TBD
```


### Examples

1. GeoDistance slider with all the default props

2. GeoDistance slider with a title

3. GeoDistance slider with range labels

4. Playground (with all knob actions)

