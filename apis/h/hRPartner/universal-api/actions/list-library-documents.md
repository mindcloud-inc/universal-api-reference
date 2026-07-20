# HR Partner: List Library Documents



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-library-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-library-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-library-documents?${params}`, {
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
      "categoryName": "Ava Chen",
      "categorySlug": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "size": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryName` | string |  |
| `categorySlug` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `size` | number |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /library` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-library-documents.md) for the provider-specific parameters and requirements.

