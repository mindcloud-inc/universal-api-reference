# RAYNET CRM: List Products



```
GET https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RAYNET CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-products?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "cost": 1,
      "id": 1,
      "name": "Ava Chen",
      "price": 1,
      "primaryPriceListItem": {
        "id": 1,
        "price": 1,
        "priceList": {
          "currency": "string"
        }
      },
      "rowInfo": {
        "createdAt": "string",
        "updatedAt": "string"
      },
      "taxRate": 1,
      "unit": "string",
      "validFrom": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Product code. |
| `cost` | number | Product cost. |
| `id` | number | Raynet product identifier. |
| `name` | string | Product name. |
| `price` | number | Product base price. |
| `primaryPriceListItem.id` | number | Primary price list item identifier. |
| `primaryPriceListItem.price` | number | Primary price list price. |
| `primaryPriceListItem.priceList.currency` | string | Primary price list currency. |
| `rowInfo.createdAt` | string | Record creation timestamp. |
| `rowInfo.updatedAt` | string | Record update timestamp. |
| `taxRate` | number | Product tax rate. |
| `unit` | string | Product unit. |
| `validFrom` | date | Product validity start date. |

## Native endpoint

Through the native RAYNET CRM API, this operation is `GET product/` (base URL `https://app.raynetcrm.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

