# <img src="https://images.mindcloud.co/apps/icons/gmod-store_1776279668074.png" alt="GmodStore logo" width="28" height="28"> GmodStore: Universal API

Access GmodStore marketplace teams, products, media, reviews, versions, users, and related commerce resources through the official Pivity API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gmodStore/latest
- **Category:** Commerce
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.gmodstore.com
- **Vendor API docs:** https://docs.pivity.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gmodStore/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Current User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current authenticated user, token metadata, and tenant context from GmodStore. |

