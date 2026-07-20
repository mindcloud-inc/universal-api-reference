# ProductLift: Create Or Update Product Vision



```
PUT https://connect.mindcloud.co/v1/universal/productLift/latest/actions/create-or-update-product-vision
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProductLift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/productLift/latest/actions/create-or-update-product-vision" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productLift/latest/actions/create-or-update-product-vision', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `id` | string |  |
| `title` | string |  |

## Native endpoint

Through the native ProductLift API, this operation is `POST /product-vision` (base URL `https://mindcloud.productlift.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-product-vision.md) for the provider-specific parameters and requirements.

