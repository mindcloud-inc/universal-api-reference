# Freepik: Download Sound Effect



```
GET https://connect.mindcloud.co/v1/universal/freepik/latest/actions/download-sound-effect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freepik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/download-sound-effect?connectionId=$CONNECTION_ID&sfxId=582" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sfxId": "582"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freepik/latest/actions/download-sound-effect?${params}`, {
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
| `sfxId` | number | yes | Freepik sound effect identifier to download. Default: `582`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "download_url": "https://example.com",
      "id": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `download_url` | string | Sound effect download URL. |
| `id` | number | Sound effect ID. |
| `title` | string | Sound effect title. |

## Native endpoint

Through the native Freepik API, this operation is `GET /v1/sound-effects/{{sfx-id}}/download` (base URL `https://api.freepik.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-sound-effect.md) for the provider-specific parameters and requirements.

