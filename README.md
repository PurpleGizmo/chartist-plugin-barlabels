# chartist-plugin-barlabels

[Chartist-js](https://github.com/gionkunz/chartist-js) Plugin for labelling the end of bars in Bar Charts.


##Usage

##### Default Options

There are two sets of default options depending on if the chart.options has horizontalBars set to true or false.

```javascript
// if chart.options.horizontalBars == true

var defaultOptions = {
  labelClass: 'ct-label',
  labelInterpolationFnc: Chartist.noop,
  labelOffset: {
    x: 2,
    y: 4
  },
  textAnchor: 'start'
}
```

```javascript
// if chart.options.horizontalBars == false / undefined

var defaultOptions = {
  labelClass: 'ct-label',
  labelInterpolationFnc: Chartist.noop,
  labelOffset: {
    x: 0,
    y: -2
  },
  textAnchor: 'middle'
}
```

##### Example Script

```javascript
new Chartist.Bar('#test-bar-chart', {
    labels: ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday'],
    series: [
      [5, 4, 3, 7, 5, 10, 3],
      [1, 2, 3, 4, 5, 6, 7]
    ]
  }, {
    seriesBarDistance: 10,
    reverseData: true,
    horizontalBars: true,
    axisY: {
      offset: 70
    },
    plugins: [
      Chartist.plugins.ctBarLabels()
    ]
  });
```

##### Example Screenshot
![Example Graph](http://i.imgur.com/RJcOkJM.png)