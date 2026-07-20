# Open Letter Connect: Get Product Types

Retrieves product types from Open Letter Connect.

```
GET https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-product-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Letter Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-product-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-product-types?${params}`, {
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
      "id": "string",
      "productType": "string",
      "size": [
        {
          "id": "string",
          "size": "string"
        }
      ],
      "windowed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `productType` | string |  |
| `size[].id` | string |  |
| `size[].size` | string |  |
| `windowed` | boolean |  |

## Native endpoint

Through the native Open Letter Connect API, this operation is `GET /products/types` (base URL `https://api.openletterconnect.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-types.md) for the provider-specific parameters and requirements.

