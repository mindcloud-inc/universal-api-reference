# <img src="https://images.mindcloud.co/apps/icons/images-14_1774869269991.jpeg" alt="BetterContact logo" width="28" height="28"> BetterContact: Universal API

BetterContact enriches contact and lead records with waterfall email and phone discovery, lead-finder searches, and account credit visibility.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/betterContact/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bettercontact.rocks
- **Vendor API docs:** https://doc.bettercontact.rocks/api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Credit Balance](actions/check-credit-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/check-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Check Credit Balance](actions/check-credit-balance.md) | GET | Retrieves the current BetterContact credit balance and account email. |

### Enrichment Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Enrichment](actions/create-enrichment.md) | POST | Creates an asynchronous BetterContact contact enrichment request. |

### Enrichment Results

| Action | Method | Description |
| --- | --- | --- |
| [Get Enrichment Results](actions/get-enrichment-results.md) | GET | Retrieves BetterContact enrichment results by request ID. |

### Lead Finder Search

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead Finder Search](actions/create-lead-finder-search.md) | POST | Creates an asynchronous BetterContact lead finder search. |

### Lead Finder Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Get Lead Finder Search Results](actions/get-lead-finder-search-results.md) | GET | Retrieves BetterContact lead finder search results by request ID. |

