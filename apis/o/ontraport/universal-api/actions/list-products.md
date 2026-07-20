# Ontraport: List Products

Retrieves a list of products from Ontraport.

```
GET https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ontraport `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/list-products?${params}`, {
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
      "date": "2026-05-07T12:00:00.000Z",
      "deleted": "string",
      "description": "string",
      "dlm": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "id": "string",
      "internalName": "Ava Chen",
      "name": "Ava Chen",
      "price": "string",
      "productCode": "string",
      "productGroup": "string",
      "sku": "string",
      "stripeProductCode": "string",
      "taxable": "string",
      "totalIncome": "string",
      "totalPurchases": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `deleted` | string |  |
| `description` | string |  |
| `dlm` | date |  |
| `externalId` | string |  |
| `id` | string |  |
| `internalName` | string |  |
| `name` | string |  |
| `price` | string |  |
| `productCode` | string |  |
| `productGroup` | string |  |
| `sku` | string |  |
| `stripeProductCode` | string |  |
| `taxable` | string |  |
| `totalIncome` | string |  |
| `totalPurchases` | string |  |

## Native endpoint

Through the native Ontraport API, this operation is `GET /Products` (base URL `https://api.ontraport.com/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

