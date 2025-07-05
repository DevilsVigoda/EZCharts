# EZChartJS

A lightweight and easy-to-use JavaScript charting library for creating line, bar, and pie charts using the HTML5 Canvas API.

---

## 📦 Features

- **Simple API**: Easy to integrate and use with minimal configuration.
- **Responsive Design**: Automatically adjusts to container size.
- **Customizable**: Change colors, fonts, labels, and more.
- **Three Chart Types Supported**:
  - Line Charts
  - Bar Charts
  - Pie Charts
- **Legend Support**: Auto-generates legends for multi-dataset visualizations.
- **No Dependencies**: Works out of the box with vanilla JavaScript.

---

## 🧩 Installation

Since this is a lightweight class-based solution, simply copy the `EZChartJS` class into your project or include it via a script tag in your HTML file.

---

## ✨ Usage Example

### HTML

```html
<div id="chartContainer" style="width: 100%; height: 400px;"></div>
```
### JS

```JavaScript
// Initialize and draw a chart
const chart = new EZChartJS('chartContainer', {
  type: 'line',
  title: 'Sample Chart'
});

chart.draw({
  labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May'],
  datasets: [
    {
      label: 'Sales',
      data: [120, 190, 170, 220, 180],
      color: '#3366cc'
    }
  ]
});
```

### Line Chart

```JavaScript
new EZChartJS('chartContainer', { type: 'line' }).draw({
  labels: ['Q1', 'Q2', 'Q3', 'Q4'],
  datasets: [
    { label: '2022', data: [100, 120, 90, 150] },
    { label: '2023', data: [120, 140, 110, 180] }
  ]
});
```

### Bar Chart

```JavaScript
new EZChartJS('chartContainer', { type: 'bar' }).draw({
  labels: ['Apples', 'Oranges', 'Bananas'],
  datasets: [
    { label: 'Sales', data: [65, 59, 80] }
  ]
});
```

### Pie Chart

```JavaScript
new EZChartJS('chartContainer', { type: 'pie' }).draw({
  labels: ['Red', 'Blue', 'Yellow'],
  datasets: [
    { data: [300, 50, 100] }
  ]
});
```

# Class options

| Option | Type | Default | Description |
| --- | --- | --- | --- |
| `type` | `string` | `'line'` | Chart type (`'line'`, `'bar'`, or `'pie'`) |
| `title` | `string` | `''` | Chart title text |
| `backgroundColor` | `string` | `'#ffffff'` | Background color of chart area |
| `responsive` | `boolean` | `true` | Whether chart should **automatically resize** with container |
| `width` | `number` | `600` | Fixed width (when `responsive=false`) |
| `height` | `number` | `400` | Fixed height (when `responsive=false`) |
| `axisColor` | `string` | `'#cccccc'` | Color of x/y axes |
| `axisWidth` | `number` | `1` | Stroke width of axes |
| `lineWidth` | `number` | `2` | Stroke width for **line charts** |
| `pointRadius` | `number` | `4` | Radius of data points in line charts |
| `labelFont` | `string` | `'12px Arial'` | Font for axis labels |
| `labelColor` | `string` | `'#666666'` | Color for axis labels |
| `titleFont` | `string` | `'bold 18px Arial'` | Font for chart title |
| `titleColor` | `string` | `'#333333'` | Color for chart title |
| `legendFont` | `string` | `'12px Arial'` | Font for legend text |
| `legendColor` | `string` | `'#333333'` | Color for legend text |
| `hideLegend` | `boolean` | `false` | Set `true` to **hide legend** |
| `showValues` | `boolean` | `false` | Show values above bars (**bar charts only**) |
| `compactLabels` | `boolean` | `false` | Use percentage-only labels (**pie charts only**) |
