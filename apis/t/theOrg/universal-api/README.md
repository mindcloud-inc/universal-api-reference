# <img src="https://images.mindcloud.co/apps/icons/the-org_1774979153340.png" alt="The Org logo" width="28" height="28"> The Org: Universal API

Search company org charts, managers, and position data from The Org

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/theOrg/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://theorg.com/
- **Vendor API docs:** https://developers.theorg.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Usage](actions/get-current-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/get-current-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Credit Usage Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Estimate Position Search Credit Usage](actions/estimate-position-search-credit-usage.md) | GET | Estimates position search credit usage in The Org. |

### Historical Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Historical Usage](actions/get-historical-usage.md) | GET | Retrieves historical API usage from The Org. |

### Manager

| Action | Method | Description |
| --- | --- | --- |
| [Find Manager](actions/find-manager.md) | GET | Finds a manager in The Org by email or LinkedIn URL. |

### Position Search

| Action | Method | Description |
| --- | --- | --- |
| [Find Positions](actions/find-positions.md) | GET | Finds positions in The Org by search filters. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Usage](actions/get-current-usage.md) | GET | Retrieves current API usage from The Org. |

