# <img src="https://images.mindcloud.co/apps/icons/umami_1777055953919.png" alt="Umami logo" width="28" height="28"> Umami: Universal API

Manage websites and analyze traffic, events, and visitor sessions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/umami/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://umami.is
- **Vendor API docs:** https://docs.umami.is/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Websites](actions/list-websites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/list-websites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Active Visitor Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [Get Active Visitors](actions/get-active-visitors.md) | GET |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET |  |

### Event Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Data](actions/get-event-data.md) | GET |  |
| [List Event Data](actions/list-event-data.md) | GET |  |

### Event Data Breakdown

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Data Events](actions/get-event-data-events.md) | GET |  |

### Event Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Series](actions/get-event-series.md) | GET |  |

### Event Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Stats](actions/get-event-stats.md) | GET |  |

### Pageview Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Website Pageviews](actions/get-website-pageviews.md) | GET |  |

### Realtime Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [Get Realtime](actions/get-realtime.md) | GET |  |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Get Session](actions/get-session.md) | GET |  |
| [List Sessions](actions/list-sessions.md) | GET |  |

### Session Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Session Activity](actions/get-session-activity.md) | GET |  |

### Session Property

| Action | Method | Description |
| --- | --- | --- |
| [List Session Properties](actions/list-session-properties.md) | GET |  |

### Session Property Value

| Action | Method | Description |
| --- | --- | --- |
| [List Session Property Values](actions/list-session-property-values.md) | GET |  |

### Session Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Session Stats](actions/get-session-stats.md) | GET |  |

### Website

| Action | Method | Description |
| --- | --- | --- |
| [Create Website](actions/create-website.md) | POST |  |
| [Get Website](actions/get-website.md) | GET |  |
| [List Websites](actions/list-websites.md) | GET |  |
| [Update Website](actions/update-website.md) | PUT |  |

### Website Date Range

| Action | Method | Description |
| --- | --- | --- |
| [Get Website Date Range](actions/get-website-date-range.md) | GET |  |

### Website Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Expanded Website Metrics](actions/get-expanded-website-metrics.md) | GET |  |
| [Get Website Metrics](actions/get-website-metrics.md) | GET |  |

### Website Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Website Stats](actions/get-website-stats.md) | GET |  |

### Weekly Session Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Weekly Sessions](actions/get-weekly-sessions.md) | GET |  |

