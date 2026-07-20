# Kiwili: Create Product

Creates a new product in Kiwili.

```
POST https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Name": "Ava Chen",
  "Price": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Name": "Ava Chen",
    "Price": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Active` | boolean | no | Whether the product is active. |
| `Name` | string | yes | The product name. |
| `Price` | number | yes | The product price. |

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

Through the native Kiwili API, this operation is `POST /product` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

