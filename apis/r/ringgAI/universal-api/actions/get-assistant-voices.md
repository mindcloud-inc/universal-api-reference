# Ringg AI: Get Assistant Voices

Retrieves assistant voices from Ringg AI.

```
GET https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-assistant-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-assistant-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-assistant-voices?${params}`, {
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
| `language` | string | no | Filter voices by language (e.g., 'en-US', 'hi-IN'). Multiple languages can be comma-separated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "voices": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "gender": "string",
          "id": "string",
          "imageUrl": "https://example.com",
          "languages": [
            "string"
          ],
          "name": "Ava Chen",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "voicePreviews": {
            "enUs": "string"
          }
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
| `voices` | array<object> |  |
| `voices[].createdAt` | date |  |
| `voices[].gender` | string |  |
| `voices[].id` | string |  |
| `voices[].imageUrl` | string |  |
| `voices[].languages` | array<string> |  |
| `voices[].name` | string |  |
| `voices[].updatedAt` | date |  |
| `voices[].voicePreviews` | object |  |
| `voices[].voicePreviews.enUs` | string |  |

## Native endpoint

Through the native Ringg AI API, this operation is `GET /agent/voices` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-assistant-voices.md) for the provider-specific parameters and requirements.

