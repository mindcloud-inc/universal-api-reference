# <img src="https://images.mindcloud.co/apps/icons/dataforb2b-icon_1775758795234.png" alt="DataForB2B logo" width="28" height="28"> DataForB2B: Universal API

Access DataForB2B's real-time company, people, enrichment, typeahead, webhook, and account APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dataForB2B/latest
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dataforb2b.ai
- **Vendor API docs:** https://docs.dataforb2b.ai/get-started/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from DataForB2B. |

### Agentic Search

| Action | Method | Description |
| --- | --- | --- |
| [Agentic Search](actions/agentic-search.md) | GET | Searches DataForB2B with a prompt. |

### Category Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Categories Typeahead](actions/categories-typeahead.md) | GET | Retrieves category suggestions from DataForB2B. |

### Company Search

| Action | Method | Description |
| --- | --- | --- |
| [Search Companies](actions/search-companies.md) | GET | Searches for companies in DataForB2B. |

### Company Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Companies Typeahead](actions/companies-typeahead.md) | GET | Retrieves company suggestions from DataForB2B. |

### Enriched Company

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Company](actions/enrich-company.md) | GET | Retrieves enriched company data from DataForB2B. |

### Enriched Profile

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Profile](actions/enrich-profile.md) | GET | Retrieves enriched profile data from DataForB2B. |

### Filter Translation

| Action | Method | Description |
| --- | --- | --- |
| [Text To Filters](actions/text-to-filters.md) | GET | Converts text into DataForB2B search filters. |

### Industry Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Industries Typeahead](actions/industries-typeahead.md) | GET | Retrieves industry suggestions from DataForB2B. |

### Location Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Locations Typeahead](actions/locations-typeahead.md) | GET | Retrieves location suggestions from DataForB2B. |

### Monitored Profile

| Action | Method | Description |
| --- | --- | --- |
| [Add Profiles To Monitor](actions/add-profiles-to-monitor.md) | PUT | Adds profiles to monitoring in DataForB2B. |
| [Remove Profiles From Monitoring](actions/remove-profiles-from-monitoring.md) | DELETE | Removes profiles from monitoring in DataForB2B. |

### Person Search

| Action | Method | Description |
| --- | --- | --- |
| [Search People](actions/search-people.md) | GET | Searches for people in DataForB2B. |

### Webhook Event

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Events](actions/list-webhook-events.md) | GET | Retrieves webhook events from DataForB2B. |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a webhook subscription in DataForB2B. |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE | Deletes a webhook subscription from DataForB2B. |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | GET | Retrieves a webhook subscription from DataForB2B. |

