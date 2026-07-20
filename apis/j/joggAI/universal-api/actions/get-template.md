# JoggAI: Get Template



```
GET https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/get-template?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/get-template?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aspectRatio": 1,
      "coverUrl": "https://example.com",
      "id": 1,
      "name": "Ava Chen",
      "previewUrl": "https://example.com",
      "variables": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aspectRatio` | number | Template aspect ratio |
| `coverUrl` | string | Template cover image |
| `id` | number | Template ID |
| `name` | string | Template name |
| `previewUrl` | string | Template preview URL |
| `variables[]` | array<object> | Template variables |

## Native endpoint

Through the native JoggAI API, this operation is `GET /v2/template/custom/{id}` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

