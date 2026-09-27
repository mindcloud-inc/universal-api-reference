# Get followers analytics with ConnectSafely

Retrieve LinkedIn followers analytics for the authenticated account. Includes engagement metrics, content performance, audience insights, and growth trends. Supports various time ranges and metric filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics/followers`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get followers analytics](https://connectsafely.ai/docs/api/linkedin-analytics/get-analytics-followers-get-followers-analytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `resultType` | query | `list` | no | Type of analytics data to retrieve Accepted values: `AUDIENCES`, `CONTENT`, `ENGAGEMENT`, `GROWTH`. |
| `timeRange` | query | `list` | no | Time range for analytics data Accepted values: `past_7_days`, `past_14_days`, `past_30_days`, `past_90_days`, `past_year`, `custom`. |
| `lineChartType` | query | `list` | no | Granularity for line chart data Accepted values: `daily`, `weekly`, `monthly`. |
| `metricType` | query | `string` | no | Specific metric to retrieve |
| `startDate` | query | `string` | no | Start date for custom range (YYYY-MM-DD) |
| `endDate` | query | `string` | no | End date for custom range (YYYY-MM-DD) |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `accountId` | `string` | LinkedIn account ID used |
| `profileId` | `string` | LinkedIn profile URN |
| `isLineChart` | `boolean` | Whether line chart data was requested |
| `filters` | `object` | Filters applied to the request |
| `data` | `object` | Simplified analytics data |
| `data.summary` | `object` |  |
| `data.summary.metrics` | `array` |  |
| `data.summary.metrics[].title` | `string` | Metric title |
| `data.summary.metrics[].value` | `string` | Metric value (formatted) |
| `data.summary.metrics[].change` | `number` | Percentage change from previous period |
| `data.summary.metrics[].changeDescription` | `string` | Description of comparison period |
| `data.summary.metrics[].description` | `string` | Metric explanation |
| `data.chart` | `object` |  |
| `data.chart.title` | `string` |  |
| `data.chart.xAxisDescription` | `string` |  |
| `data.chart.yAxisDescription` | `string` |  |
| `data.chart.xValueUnit` | `string` |  |
| `data.chart.yValueUnit` | `string` |  |
| `data.chart.points` | `array` |  |
| `data.chart.points[].date` | `string` |  |
| `data.chart.points[].value` | `number` |  |
| `data.chart.points[].tooltip` | `string` |  |
| `data.chart.points[].change` | `number` |  |
| `data.availableFilters` | `array` | Available filter options for the UI |
| `data.headers` | `array` | Column headers for data display |

### Example response

```json
{
  "success": true,
  "accountId": "696ce9e780e0483585e4e553",
  "profileId": "ACoAAATPlQ0Bc8wdg-Iy8wZgEDuSdIVWJiE1Aio",
  "isLineChart": false,
  "filters": {
    "resultType": "ENGAGEMENT",
    "timeRange": "past_7_days"
  },
  "data": {
    "summary": {
      "metrics": [
        {
          "title": "Total followers",
          "value": "12,841",
          "change": 1,
          "changeDescription": "vs. prior 7 days",
          "description": "The total number of people that currently follow you."
        }
      ]
    },
    "chart": {
      "title": "New followers",
      "xValueUnit": "day",
      "yValueUnit": "New followers",
      "points": [
        {
          "date": "Feb 18",
          "value": 9,
          "tooltip": "Wednesday, Feb 18, 2026",
          "change": null
        },
        {
          "date": "Feb 19",
          "value": 16,
          "tooltip": "Thursday, Feb 19, 2026",
          "change": 77.8
        },
        {
          "date": "Feb 20",
          "value": 25,
          "tooltip": "Friday, Feb 20, 2026",
          "change": 56.3
        }
      ]
    }
  }
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
