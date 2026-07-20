# Fourthwall: Get Product Inventory

Retrieves product inventory from Fourthwall by product ID.

```
GET https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-product-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fourthwall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-product-inventory?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-product-inventory?${params}`, {
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
| `productId` | string | yes | The product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "quantity": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "variantId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `quantity` | number |  |
| `updatedAt` | date |  |
| `variantId` | string |  |

## Native endpoint

Through the native Fourthwall API, this operation is `GET /open-api/v1.0/products/:productId/inventory` (base URL `https://api.fourthwall.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-inventory.md) for the provider-specific parameters and requirements.

