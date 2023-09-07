<p align="center">
    <img height="250" src="https://raw.githubusercontent.com/clydescobidal/svelte-sbchart/main/images/svelte-sbchart.png?v=1.0.0" alt="Svelte SBChart"><br/>
    A simple and lightweight baseline charting package for Svelte
</p>

<p align="center">
    <a href="https://www.npmjs.com/package/svelte-sbchart"><img src="https://badge.fury.io/js/svelte-sbchart.svg?v=1.0.4" alt="NPM Package"></a>
    <img src="https://github.com/clydescobidal/svelte-sbchart/actions/workflows/build.yml/badge.svg" alt="Build">
    <img src="https://img.shields.io/npm/l/svelte-sbchart" alt="License">
    <img src="https://img.shields.io/npm/dm/svelte-sbchart" alt="Monthly downloads">
    <img src="https://img.shields.io/npm/dt/svelte-sbchart" alt="Total downloads">
</p>


![Alt text](https://raw.githubusercontent.com/clydescobidal/svelte-sbchart/main/images/svelte-sbchart-preview.png "svelte-sbchart")


## Installation

```
npm install svelte-sbchart
```

## Usage

### A basic usage

```html
<template>
    <div style="width: 500px; height: 230px">
        <SvelteSBChart {series} {baseValue} {options} />
    </div>
</template>
```

```javascript
import { SvelteSBChart } from 'svelte-sbchart';

const series = [
    { timestamp: 1656818225, value: 12 },
    { timestamp: 1656818226, value: 13 },
    { timestamp: 1656818227, value: 14 },
    { timestamp: 1656818228, value: 15 },
    { timestamp: 1656818229, value: 12.5 },
    { timestamp: 1656818230, value: 13 },
    { timestamp: 1656818231, value: 12 }
];
const baseValue = 13;
const options = {
    upColor: '#37eb34',
    downColor: '#eb3434',
    lineWidth: 1
};
```

### Props
| Property      | Type |  Description |
| ----------- |  ---- | ---
| series      | Array       | An array of objects containing **value** and **UNIX timestamp** properties
| baseValue   | float       | The base value used to calculate high and low positions
| options   | Object        | An object with customization properties (see below)
| interactive   | Boolean       | Show pop-up on hover (default: **true**) 
| gridLines   | Boolean       | Enable grid lines background (default: **true**) 

### Options
You can customize the chart by passing an object in the component's **options** prop (see example above) with these properties:
| Property      | Type | Default | Description |
| ----------- | ----------- | ---- | ---
| upColor      | string (hex)       | #008000 | Gradient and line color when value is higher than the base value
| downColor   | string (hex)        | #ff0000 | Gradient and line color when value is less than the base value
| lineWidth   | Number        | 1  | The line size of stroke


### License
MIT © [Clyde Escobidal](https://clydescobidal.dev)
