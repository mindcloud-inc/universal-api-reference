# <img src="https://images.mindcloud.co/apps/icons/lead-iq_1774389785472.png" alt="LeadIQ logo" width="28" height="28"> LeadIQ: Universal API

Search and enrich people and company data with LeadIQ

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/leadIQ/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://leadiq.com
- **Vendor API docs:** https://developer.leadiq.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Grouped Advanced Search](actions/grouped-advanced-search.md) | GET |  |
| [Search Company](actions/search-company.md) | GET |  |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Flat Advanced Search](actions/flat-advanced-search.md) | GET |  |
| [Search People](actions/search-people.md) | GET |  |
| [Submit Person Feedback](actions/submit-person-feedback.md) | PUT |  |

