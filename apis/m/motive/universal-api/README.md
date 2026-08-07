# <img src="https://images.mindcloud.co/apps/icons/motive-app-logo_1786040116277.png" alt="Motive logo" width="28" height="28"> Motive: Universal API

Motive fleet management endpoints for the Kendall job-backed data pulls: assets, vehicles, users, driver performance events, scorecard summary, driver utilization, and vehicle utilization.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/motive/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gomotive.com/
- **Vendor API docs:** https://developer.gomotive.com/reference/getting-started-with-your-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List assets](actions/list-assets.md) | GET |  |
| [List driver performance events](actions/list-driver-performance-events.md) | GET |  |
| [List driver utilization](actions/list-driver-utilization.md) | GET |  |
| [List scorecard summaries](actions/list-scorecard-summaries.md) | GET |  |
| [List users](actions/list-users.md) | GET |  |
| [List vehicle utilization](actions/list-vehicle-utilization.md) | GET |  |
| [List vehicles](actions/list-vehicles.md) | GET |  |

