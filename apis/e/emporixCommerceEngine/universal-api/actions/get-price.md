# Emporix Commerce Engine: Get Price

Retrieves a price from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-price?connectionId=$CONNECTION_ID&priceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "priceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-price?${params}`, {
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
| `priceId` | string | yes | The unique ID of the price. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "id": "string",
      "itemYrn": "string",
      "metadata": {},
      "mixins": {},
      "priceModel": {},
      "priceModelId": "string",
      "salePrice": {},
      "tierValues": [
        {}
      ],
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `id` | string |  |
| `itemYrn` | string |  |
| `metadata` | object |  |
| `mixins` | object |  |
| `priceModel` | object |  |
| `priceModelId` | string |  |
| `salePrice` | object |  |
| `tierValues` | array<object> |  |
| `vendorId` | string |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `GET /price/{{credentials.tenantId}}/prices/:priceId` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-price.md) for the provider-specific parameters and requirements.

