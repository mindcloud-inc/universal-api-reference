# Stencil: Search Images



```
GET https://connect.mindcloud.co/v1/universal/stencil/latest/actions/search-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stencil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stencil/latest/actions/search-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stencil/latest/actions/search-images?${params}`, {
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
| `q` | string | no | Case-insensitive search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "imageUrl": "https://example.com",
      "imageUrlJpg": "https://example.com",
      "log": "string",
      "metadata": {},
      "modifications": [
        {}
      ],
      "self": "string",
      "status": "string",
      "templateId": "string",
      "webhookResponseBody": "string",
      "webhookResponseCode": 1,
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `imageUrlJpg` | string |  |
| `log` | string |  |
| `metadata` | object |  |
| `modifications` | array<object> |  |
| `self` | string |  |
| `status` | string |  |
| `templateId` | string |  |
| `webhookResponseBody` | string |  |
| `webhookResponseCode` | number |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Stencil API, this operation is `POST /v1/images/search` (base URL `https://api.usestencil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-images.md) for the provider-specific parameters and requirements.

