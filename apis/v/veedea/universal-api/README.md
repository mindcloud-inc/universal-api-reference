# <img src="https://images.mindcloud.co/apps/icons/veedea-icon_1775684874101.jpeg" alt="Veedea logo" width="28" height="28"> Veedea: Universal API

Create video funnels and manage campaigns, leads, and purchases

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/veedea/latest
- **Category:** Communication / Video Communications
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://veedea.com
- **Vendor API docs:** https://veedea.com/api/doc

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Auth Token](actions/get-auth-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veedea/latest/actions/get-auth-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Auth Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Auth Token](actions/get-auth-token.md) | GET | Retrieves an auth token from Veedea. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves all campaign records from Veedea. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [List Leads](actions/list-leads.md) | GET | Retrieves all lead records from Veedea. |

