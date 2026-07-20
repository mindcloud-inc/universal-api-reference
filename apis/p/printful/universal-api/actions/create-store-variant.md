# Printful: Create Store Variant

Creates a new sync variant in a Printful store.

```
POST https://connect.mindcloud.co/v1/universal/printful/latest/actions/create-store-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printful/latest/actions/create-store-variant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printful/latest/actions/create-store-variant', {
  method: 'POST',
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
      "retail_price": "string"
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
| `retail_price` | string |  |

## Native endpoint

Through the native Printful API, this operation is `POST /store/products/{id}/variants` (base URL `https://api.printful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-store-variant.md) for the provider-specific parameters and requirements.

