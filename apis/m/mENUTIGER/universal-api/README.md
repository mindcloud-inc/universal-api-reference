# <img src="https://images.mindcloud.co/apps/icons/favicon_1775068989696.png" alt="MENU TIGER logo" width="28" height="28"> MENU TIGER: Universal API

Access MENU TIGER Zapier integration data such as restaurant status, orders, and customers using a MENU TIGER developer API key.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mENUTIGER/latest
- **Category:** Commerce
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.menutiger.com/
- **Vendor API docs:** https://menutiger.helpscoutdocs.com/article/41-how-to-integrate-zapier-to-menu-tiger

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Integration Status](actions/get-integration-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mENUTIGER/latest/actions/get-integration-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [List Orders](actions/list-orders.md) | GET |  |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Integration Status](actions/get-integration-status.md) | GET |  |

