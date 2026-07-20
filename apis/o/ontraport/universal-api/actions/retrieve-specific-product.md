# Ontraport: Retrieve Specific Product

Retrieves a specific product from Ontraport.

```
GET https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/retrieve-specific-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ontraport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/retrieve-specific-product?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/retrieve-specific-product?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The product ID. |

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

Through the native Ontraport API, this operation is `GET /Product` (base URL `https://api.ontraport.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-specific-product.md) for the provider-specific parameters and requirements.

