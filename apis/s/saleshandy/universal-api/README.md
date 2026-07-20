# <img src="https://images.mindcloud.co/apps/icons/favicon-27_1777311129194.png" alt="Saleshandy logo" width="28" height="28"> Saleshandy: Universal API

Manage prospects, sequences, email outreach, and campaign analytics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/saleshandy/latest
- **Category:** Marketing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.saleshandy.com/
- **Vendor API docs:** https://developer.saleshandy.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sequences](actions/list-sequences.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/list-sequences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET |  |

### Dnc Item

| Action | Method | Description |
| --- | --- | --- |
| [Get DNC List Items](actions/get-dnc-list-items.md) | GET |  |
| [Search DNC Items](actions/search-dnc-items.md) | GET |  |

### Dnc List

| Action | Method | Description |
| --- | --- | --- |
| [List DNC Lists](actions/list-dnc-lists.md) | GET |  |

### Enrich Rate Limits

| Action | Method | Description |
| --- | --- | --- |
| [Get Enrich Rate Limits](actions/get-enrich-rate-limits.md) | GET |  |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [List Fields](actions/list-fields.md) | GET |  |

### Prospect

| Action | Method | Description |
| --- | --- | --- |
| [List Prospects](actions/list-prospects.md) | GET |  |

### Prospect Sequence History

| Action | Method | Description |
| --- | --- | --- |
| [Get Prospect Minimal Sequences](actions/get-prospect-minimal-sequences.md) | GET |  |

### Prospect Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Prospect Tags](actions/list-prospect-tags.md) | GET |  |

### Prospect Verification Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Prospect Verification Status](actions/get-prospect-verification-status.md) | GET |  |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Schedules](actions/list-schedules.md) | GET |  |

### Sequence

| Action | Method | Description |
| --- | --- | --- |
| [Create Sequence](actions/create-sequence.md) | POST |  |
| [List Sequences](actions/list-sequences.md) | GET |  |

### Sequence Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Update Sequence Schedule](actions/update-sequence-schedule.md) | PUT |  |

### Sequence Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Sequence Settings](actions/get-sequence-settings.md) | GET |  |

### Sequence Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Sequence Stats](actions/get-sequence-stats.md) | GET |  |

### Sequence Step

| Action | Method | Description |
| --- | --- | --- |
| [List Sequence Steps](actions/list-sequence-steps.md) | GET |  |

### Sequence Step Variant

| Action | Method | Description |
| --- | --- | --- |
| [Get Sequence Step Variants](actions/get-sequence-step-variants.md) | GET |  |

### Task Counts

| Action | Method | Description |
| --- | --- | --- |
| [Get Task Counts](actions/get-task-counts.md) | GET |  |

### Team Member

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members](actions/list-team-members.md) | GET |  |

