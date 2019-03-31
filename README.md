vue-emitting-analog-clock
========

#### emitting analog clock component for vuejs ####
Vue wrapper of [emitting-analog-clock](https://moritanian.github.io/emitting-analog-clock)

<a href="https://moritanian.github.io/emitting-analog-clock"><img src="https://moritanian.github.io/emitting-analog-clock/sample.png"/></a>


<p align="center"><a href="https://moritanian.github.io/emitting-analog-clock">DEMO</a></p>

## Props
| Prop    | Type | Default | Usage  |
| ------  | ---- | --- | ----- | ------ |
| id   | String | 'clock' | id attribute of the dom element |
| shape | String | 'circle' | Shape of the clock. 'square' and 'circle' can be selected. |
| size | Number | 200 | Size of the clock in pixels. |
| color | String | '#28d1fa' | Color of the clock. |
| backgroundColor | String | '#09303aff' | Background color of the clock. |
| backgroundImage | String | null | Background image url. |
| visibleSecondHand | Boolean | true | Set true to show the second hand. |
| shadowing | Boolean | true | Set true to show the shadow of the clock. |
| showDigital | Boolean | false | Set true to show the text of the time in the clock. |
| smooth | Boolean | false | Set true to move hands smoothly. |
| date | Object | null | Show stopped clock. The value should be Date object or the string that represents the date. |
| dateFunc | Function (date: Date) => Date | now => now | Lambda that gets the current Date object and returns the Date object to show. |
| nextFunc | Function (date: Date) => Number | date => ((1500 - date.getMilliseconds()) % 1000) + 500, | Lambda that gets the current Date object and returns the next rendering time in ms. |


## Usage
```demo.vue
<template>
    <emitting-analog-clock id='main-clock' :size='260' :showDigital="true"></emitting-analog-clock>
</template>
<script>
import EmittingAnalogClock from 'vue-emitting-analog-clock';
export default {
  components: {EmittingAnalogClock}
};
</script>
```
