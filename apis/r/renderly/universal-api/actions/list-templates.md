# Renderly: List Templates

Retrieves available video templates from Renderly.

```
GET https://connect.mindcloud.co/v1/universal/renderly/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Renderly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/renderly/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/renderly/latest/actions/list-templates?${params}`, {
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
      "category": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditsPerMinute": 1,
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "previewVideoUrl": "https://example.com",
      "thumbnailUrl": "https://example.com",
      "variables": [
        {
          "defaultValue": "string",
          "name": "Ava Chen",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `createdAt` | date |  |
| `creditsPerMinute` | number |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `previewVideoUrl` | string |  |
| `thumbnailUrl` | string |  |
| `variables` | array<object> |  |
| `variables[].defaultValue` | string |  |
| `variables[].name` | string |  |
| `variables[].type` | string |  |

## Native endpoint

Through the native Renderly API, this operation is `GET /templates` (base URL `https://renderly.video/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

