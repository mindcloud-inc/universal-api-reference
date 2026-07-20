# Colossyan: List Avatars

Retrieves available avatars from Colossyan.

```
GET https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/list-avatars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Colossyan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/list-avatars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/list-avatars?${params}`, {
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
      "age": 1,
      "clothing_style": "string",
      "default_voice": "string",
      "display_name": "Ava Chen",
      "emotions": [
        {}
      ],
      "ethnicity": "string",
      "features": {},
      "gender": "string",
      "name": "Ava Chen",
      "preview_url": "https://example.com",
      "quality": "string",
      "type": "string",
      "version": "string",
      "views": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | number | Approximate avatar age when provided. |
| `clothing_style` | string | Avatar clothing style label. |
| `default_voice` | string | Default voice identifier for the avatar. |
| `display_name` | string | Human-readable avatar name. |
| `emotions` | array<object> | Supported emotions when available. |
| `ethnicity` | string | Avatar ethnicity label when provided. |
| `features` | object | Capability flags for the avatar. |
| `gender` | string | Avatar gender. |
| `name` | string | Avatar identifier. |
| `preview_url` | string | Preview video URL for the avatar. |
| `quality` | string | Avatar quality tier. |
| `type` | string | Avatar type. |
| `version` | string | Avatar version. |
| `views` | array<object> | Available view variants and preview assets for the avatar. |

## Native endpoint

Through the native Colossyan API, this operation is `GET /assets/actors` (base URL `https://app.colossyan.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-avatars.md) for the provider-specific parameters and requirements.

