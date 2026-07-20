# <img src="https://images.mindcloud.co/apps/icons/image-charts_1775223432902.png" alt="Image-Charts logo" width="28" height="28"> Image-Charts: Universal API

Generate charts, GraphViz graphs, QR codes, and Chart.js images

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/imageCharts/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.image-charts.com/
- **Vendor API docs:** https://documentation.image-charts.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Create Base64-Encoded Chart.js Image Chart](actions/create-base64-encoded-chart-js-image-chart.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imageCharts/latest/actions/create-base64-encoded-chart-js-image-chart?connectionId=$CONNECTION_ID&chart=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Chart Image

| Action | Method | Description |
| --- | --- | --- |
| [Create Base64-Encoded Chart.js Image Chart](actions/create-base64-encoded-chart-js-image-chart.md) | GET | Creates a Base64-encoded Chart.js image chart with Image-Charts. |
| [Create Bubble Chart](actions/create-bubble-chart.md) | GET | Creates a bubble chart with Image-Charts. |
| [Create Chart.js Image Chart](actions/create-chart-js-image-chart.md) | GET | Creates a Chart.js image chart with Image-Charts. |
| [Create Concentric Pie Chart](actions/create-concentric-pie-chart.md) | GET | Creates a concentric pie chart with Image-Charts. |
| [Create Doughnut Chart](actions/create-doughnut-chart.md) | GET | Creates a doughnut chart with Image-Charts. |
| [Create Doughnut Chart With Inside Label](actions/create-doughnut-chart-with-inside-label.md) | GET | Creates a doughnut chart with an inside label using Image-Charts. |
| [Create Gradient Progress Bar Chart](actions/create-gradient-progress-bar-chart.md) | GET | Creates a gradient progress bar chart with Image-Charts. |
| [Create Grouped Horizontal Bar Chart](actions/create-grouped-horizontal-bar-chart.md) | GET | Creates a grouped horizontal bar chart with Image-Charts. |
| [Create Grouped Vertical Bar Chart](actions/create-grouped-vertical-bar-chart.md) | GET | Creates a grouped vertical bar chart with Image-Charts. |
| [Create Line Chart](actions/create-line-chart.md) | GET | Creates a line chart with Image-Charts. |
| [Create Multi-Color Progress Bar Chart](actions/create-multi-color-progress-bar-chart.md) | GET | Creates a multi-color progress bar chart with Image-Charts. |
| [Create Multi-Series Line Chart](actions/create-multi-series-line-chart.md) | GET | Creates a multi-series line chart with Image-Charts. |
| [Create Pie Chart](actions/create-pie-chart.md) | GET | Creates a pie chart with Image-Charts. |
| [Create Pie Chart With Labels](actions/create-pie-chart-with-labels.md) | GET | Creates a labeled pie chart with Image-Charts. |
| [Create Pie Chart With Legend](actions/create-pie-chart-with-legend.md) | GET | Creates a pie chart with a legend with Image-Charts. |
| [Create Polar Area Chart](actions/create-polar-area-chart.md) | GET | Creates a polar area chart with Image-Charts. |
| [Create Polar Area Chart With Slice Gradients](actions/create-polar-area-chart-with-slice-gradients.md) | GET | Creates a polar area chart with slice gradients in Image-Charts. |
| [Create QR Code SVG](actions/create-qr-code-svg.md) | GET | Creates an SVG QR code image with Image-Charts. |
| [Create Radar Chart](actions/create-radar-chart.md) | GET | Creates a radar chart with Image-Charts. |
| [Create Radar Chart With Open Path](actions/create-radar-chart-with-open-path.md) | GET | Creates an open-path radar chart with Image-Charts. |
| [Create Scatter Chart](actions/create-scatter-chart.md) | GET | Creates a scatter chart with Image-Charts. |
| [Create Simple Progress Bar Chart](actions/create-simple-progress-bar-chart.md) | GET | Creates a simple progress bar chart with Image-Charts. |
| [Create Sparkline Chart](actions/create-sparkline-chart.md) | GET | Creates a sparkline chart with Image-Charts. |
| [Create Stacked Horizontal Bar Chart](actions/create-stacked-horizontal-bar-chart.md) | GET | Creates a stacked horizontal bar chart with Image-Charts. |
| [Create Stacked Vertical Bar Chart](actions/create-stacked-vertical-bar-chart.md) | GET | Creates a stacked vertical bar chart with Image-Charts. |

### Graph Image

| Action | Method | Description |
| --- | --- | --- |
| [Create GraphViz Circo Layout](actions/create-graphviz-circo-layout.md) | GET | Creates a GraphViz Circo layout with Image-Charts. |
| [Create GraphViz Digraph](actions/create-graphviz-digraph.md) | GET | Creates a GraphViz digraph with Image-Charts. |
| [Create GraphViz Graph](actions/create-graphviz-graph.md) | GET | Creates a GraphViz graph with Image-Charts. |
| [Create GraphViz Subgraph Layout](actions/create-graphviz-subgraph-layout.md) | GET | Creates a GraphViz subgraph layout with Image-Charts. |

### Qr Code Image

| Action | Method | Description |
| --- | --- | --- |
| [Create QR Code](actions/create-qr-code.md) | GET | Creates a QR code image with Image-Charts. |

