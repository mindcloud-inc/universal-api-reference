# <img src="https://images.mindcloud.co/apps/icons/images-10_1775824413746.png" alt="Biyo POS logo" width="28" height="28"> Biyo POS: Universal API

Biyo POS is a point-of-sale platform with an API-key-based dashboard integration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/biyoPOS/latest
- **Category:** Commerce
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://biyopos.com/
- **Vendor API docs:** https://biyopos.com/encyclopedia/api-application-programming-interface/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Categories](actions/list-categories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/biyoPOS/latest/actions/list-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves category records from Biyo POS. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET | Retrieves customer records from Biyo POS. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [List Orders](actions/list-orders.md) | GET | Retrieves order records from Biyo POS. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves product records from Biyo POS. |

