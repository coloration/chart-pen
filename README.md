### Use

```js
const yAxisStyle = AxisStyle({
  type: 'y',
  name: 'age'
})

const xAxisStyle = AxisStyle({
  type: 'x',
  name: 'time'
})

const style = composeStyle(xAxisStyle, yAxisStyle)

// set style with Style
const barChart = style.decorate(BarChart(legend, value))
const lineChart = style.decorate(LineChart(legend, value))

const chartRender = composeChart(barChart, lineChart)
chartRender(container)

const theme = Theme({
  color: ['red', 'blue', 'yellow']
})

theme.regist(style)

// set style with Theme
const barColorChart = theme.decorate(barChart)
const lineColorChart = theme.decorate(lineChart)

const chartRender = composeChart(barColorChart, lineColorChart)
chartRender(container)
```