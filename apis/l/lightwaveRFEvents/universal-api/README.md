# <img src="https://images.mindcloud.co/apps/icons/favicon-lightwaverf-com-48x48_1777315429582.png" alt="LightwaveRF Events logo" width="28" height="28"> LightwaveRF Events: Universal API

Access LightwaveRF Smart Series event webhook subscriptions and event-related API resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lightwaveRFEvents/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lightwaverf.com
- **Vendor API docs:** https://support.lightwaverf.com/knowledge/link-plus-smart-series-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Events](actions/list-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFEvents/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves registered event webhook subscriptions from LightwaveRF Events. |

