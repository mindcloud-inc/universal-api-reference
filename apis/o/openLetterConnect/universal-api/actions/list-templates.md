# Open Letter Connect: List Templates

Retrieves templates from Open Letter Connect.

```
GET https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Letter Connect `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/list-templates?${params}`, {
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
      "creator": {
        "fullName": "Ava Chen",
        "id": "string"
      },
      "id": "string",
      "product": {
        "deliveryType": "string",
        "envelopeType": "string",
        "id": "string",
        "name": "Ava Chen",
        "paperSize": "string",
        "paperType": "string",
        "postageType": "string",
        "productType": "string"
      },
      "templateType": "string",
      "templateUrl": "https://example.com",
      "thumbnailUrl": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creator.fullName` | string |  |
| `creator.id` | string |  |
| `id` | string |  |
| `product.deliveryType` | string |  |
| `product.envelopeType` | string |  |
| `product.id` | string |  |
| `product.name` | string |  |
| `product.paperSize` | string |  |
| `product.paperType` | string |  |
| `product.postageType` | string |  |
| `product.productType` | string |  |
| `templateType` | string |  |
| `templateUrl` | string |  |
| `thumbnailUrl` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Open Letter Connect API, this operation is `GET /templates` (base URL `https://api.openletterconnect.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

