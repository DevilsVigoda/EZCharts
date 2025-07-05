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

