# Kiwili: Get Product Details

Retrieves details for a product in Kiwili.

```
GET https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-product-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-product-details?connectionId=$CONNECTION_ID&product_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "product_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-product-details?${params}`, {
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
| `product_id` | number | yes | The Kiwili product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Active": true,
      "Id": 1,
      "Name": "Ava Chen",
      "Price": 1,
      "SKU": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Active` | boolean |  |
| `Id` | number |  |
| `Name` | string |  |
| `Price` | number |  |
| `SKU` | string |  |

## Native endpoint

Through the native Kiwili API, this operation is `GET /product/:product_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-details.md) for the provider-specific parameters and requirements.

