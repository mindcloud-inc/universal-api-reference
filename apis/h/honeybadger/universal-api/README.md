# <img src="https://images.mindcloud.co/apps/icons/honeybadger_1776300875933.png" alt="Honeybadger logo" width="28" height="28"> Honeybadger: Universal API

Honeybadger lets teams report errors, deployments, check-ins, source maps, and custom events to the Honeybadger reporting endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/honeybadger/latest
- **Category:** IT Operations / Observability
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.honeybadger.io/
- **Vendor API docs:** https://docs.honeybadger.io/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Ping Check-in](actions/ping-check-in.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/ping-check-in" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checkInId": "string"
}'
```

## Actions (7)

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [Report Error](actions/report-error.md) | POST | Reports an application error to Honeybadger. |

### Deployments

| Action | Method | Description |
| --- | --- | --- |
| [Report Deployment](actions/report-deployment.md) | POST | Reports an application deployment to Honeybadger. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Report Event](actions/report-event.md) | POST | Reports monitoring events to Honeybadger Insights. |

### File Versions

| Action | Method | Description |
| --- | --- | --- |
| [Upload Source Map](actions/upload-source-map.md) | POST | Uploads a source map to Honeybadger. |

### Monitors

| Action | Method | Description |
| --- | --- | --- |
| [Ping Check-in](actions/ping-check-in.md) | POST | Reports a check-in to Honeybadger by ID. |
| [Ping Check-in by Slug](actions/ping-check-in-by-slug.md) | POST | Reports a check-in to Honeybadger by slug. |
| [Report Check-in Details](actions/report-check-in-details.md) | POST | Reports check-in details to Honeybadger by ID. |

