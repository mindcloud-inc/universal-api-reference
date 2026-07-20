# <img src="https://images.mindcloud.co/apps/icons/linkila_1778007091264.png" alt="Linkila logo" width="28" height="28"> Linkila: Universal API

Create, manage, and analyze Linkila short links, domains, filters, redirection sessions, and access logs through the Linkila Public API v1.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/linkila/latest
- **Category:** Marketing
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://linkila.com/
- **Vendor API docs:** https://app.linkila.com/integrations/api/v1/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Filters](actions/list-filters.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkila/latest/actions/list-filters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Access Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Access Log](actions/get-access-log.md) | GET | Retrieves access log entries from Linkila. |

### Analytics Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Analytics By Interval](actions/count-analytics-by-interval.md) | GET | Retrieves Linkila analytics counts by time interval. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [List Domains](actions/list-domains.md) | GET | Retrieves configured link domains from Linkila. |

### Filter

| Action | Method | Description |
| --- | --- | --- |
| [List Filters](actions/list-filters.md) | GET | Retrieves saved filters from Linkila. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Edit Link](actions/edit-link.md) | PUT | Updates an existing link in Linkila. |
| [List Links](actions/list-links.md) | GET | Retrieves saved links from Linkila. |
| [Quick Generate Link](actions/quick-generate-link.md) | POST | Creates a new link and short URL in Linkila. |

### Redirection

| Action | Method | Description |
| --- | --- | --- |
| [Get Redirection](actions/get-redirection.md) | GET | Retrieves a destination URL from Linkila and logs access. |

### Redirection Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Redirection Session](actions/create-redirection-session.md) | POST | Creates a redirection session in Linkila. |

