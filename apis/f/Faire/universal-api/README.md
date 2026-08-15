# <img src="https://images.mindcloud.co/apps/icons/faire-icon_1782393384155.png" alt="Faire logo" width="28" height="28"> Faire: Universal API

Faire through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/Faire/latest
- **Category:** Commerce
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://faire.github.io/external-api-docs/#introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Orders](actions/list-orders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/Faire/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [List a single Order](actions/list-a-single-order.md) | GET |  |
| [List Orders](actions/list-orders.md) | GET |  |
| [Update inventory by SKUs](actions/update-inventory.md) | GET |  |

