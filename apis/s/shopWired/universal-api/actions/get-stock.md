# ShopWired: Retrieve stock quantity

Retrieves stock quantities from ShopWired by SKU.

```
GET https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-stock
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShopWired `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-stock?connectionId=$CONNECTION_ID&sku=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sku": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-stock?${params}`, {
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
| `sku` | string | yes | The SKU code for the product or product variation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "quantity": 1,
      "sku": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `quantity` | number |  |
| `sku` | string |  |

## Native endpoint

Through the native ShopWired API, this operation is `GET /stock` (base URL `https://api.ecommerceapi.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stock.md) for the provider-specific parameters and requirements.

