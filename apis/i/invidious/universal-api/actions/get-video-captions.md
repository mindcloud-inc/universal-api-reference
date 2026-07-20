# Invidious: Get Video Captions



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-video-captions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-video-captions?connectionId=$CONNECTION_ID&id=dQw4w9WgXcQ" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "dQw4w9WgXcQ"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-video-captions?${params}`, {
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
| `id` | string | yes | Video ID to fetch captions for. Example: `dQw4w9WgXcQ`. |
| `label` | string | no | Caption label to fetch a selected caption track. |
| `language` | string | no | Caption language code. |
| `translationLanguage` | string | no | Target language for caption auto-translation. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `region` | string | no | ISO 3166 country code. Example: `US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "label": "string",
      "languageCode": "string",
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `label` | string |  |
| `languageCode` | string |  |
| `videoId` | string |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /captions/:id` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-captions.md) for the provider-specific parameters and requirements.

