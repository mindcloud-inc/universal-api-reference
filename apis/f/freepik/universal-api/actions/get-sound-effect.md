# Freepik: Get Sound Effect



```
GET https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-sound-effect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freepik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-sound-effect?connectionId=$CONNECTION_ID&sfxId=582" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sfxId": "582"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-sound-effect?${params}`, {
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
| `sfxId` | number | yes | Freepik sound effect identifier. Default: `582`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "download_count": 1,
      "duration": 1,
      "file_url": "https://example.com",
      "id": 1,
      "is_premium": true,
      "popularity": 1,
      "tags": [
        {}
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | object | Category details. |
| `created_at` | date | Creation timestamp. |
| `download_count` | number | Download count. |
| `duration` | number | Duration in seconds. |
| `file_url` | string | Audio file URL. |
| `id` | number | Sound effect ID. |
| `is_premium` | boolean | Whether the sound effect is premium. |
| `popularity` | number | Popularity score. |
| `tags` | array<object> | Tags. |
| `title` | string | Sound effect title. |

## Native endpoint

Through the native Freepik API, this operation is `GET /v1/sound-effects/{{sfx-id}}` (base URL `https://api.freepik.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sound-effect.md) for the provider-specific parameters and requirements.

