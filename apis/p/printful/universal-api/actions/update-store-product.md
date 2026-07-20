# Printful: Update Store Product

Updates a sync product in a Printful store.

```
PUT https://connect.mindcloud.co/v1/universal/printful/latest/actions/update-store-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/printful/latest/actions/update-store-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printful/latest/actions/update-store-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Printful sync product id. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "external_id": "string",
      "id": 1,
      "name": "Ava Chen",
      "thumbnail_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `external_id` | string |  |
| `id` | number |  |
| `name` | string |  |
| `thumbnail_url` | string |  |

## Native endpoint

Through the native Printful API, this operation is `PUT /store/products/{id}` (base URL `https://api.printful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-store-product.md) for the provider-specific parameters and requirements.

