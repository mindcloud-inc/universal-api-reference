# <img src="https://images.mindcloud.co/apps/icons/chartly-logo_1783998554589.png" alt="ChartLy logo" width="28" height="28"> ChartLy: Universal API

Generate chart images, create chart URLs, and track chart metrics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chartLy/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://chartly.dev
- **Vendor API docs:** https://docs.chartly.dev/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Status](actions/get-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chartLy/latest/actions/get-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Chart

| Action | Method | Description |
| --- | --- | --- |
| [Create Bar Chart (Zapier)](actions/create-bar-chart-zapier.md) | POST | Creates a Zapier-friendly bar chart in Chartly. |
| [Create Line Chart (Zapier)](actions/create-line-chart-zapier.md) | POST | Creates a Zapier-friendly line chart in Chartly. |
| [Create Multi-Series Chart (Zapier)](actions/create-multi-series-chart-zapier.md) | POST | Creates a Zapier-friendly multi-series chart in Chartly. |
| [Create Permanent Signed Short URL](actions/create-permanent-signed-short-url.md) | POST | Creates a permanent signed short URL in Chartly. |
| [Create Pie Chart (Zapier)](actions/create-pie-chart-zapier.md) | POST | Creates a Zapier-friendly pie chart in Chartly. |
| [Render Chart From JSON](actions/render-chart-from-json.md) | POST | Renders a chart image from JSON config in Chartly. |
| [Render Chart From URL](actions/render-chart-from-url.md) | POST | Renders a chart image from URL-encoded config in Chartly. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Status](actions/get-status.md) | GET | Retrieves Chartly API health and configuration status. |

