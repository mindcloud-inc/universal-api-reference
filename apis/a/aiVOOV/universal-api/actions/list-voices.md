# AiVOOV: List Voices

Retrieves available voice IDs from AiVOOV.

```
GET https://connect.mindcloud.co/v1/universal/aiVOOV/latest/actions/list-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AiVOOV `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aiVOOV/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aiVOOV/latest/actions/list-voices?${params}`, {
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
| `languageCode` | string | no | Filter voices by language code, for example en-US. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gender": "string",
      "label": "string",
      "languageCode": "string",
      "languageName": "Ava Chen",
      "name": "Ava Chen",
      "value": "string",
      "voiceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gender` | string |  |
| `label` | string |  |
| `languageCode` | string |  |
| `languageName` | string |  |
| `name` | string |  |
| `value` | string |  |
| `voiceId` | string |  |

## Native endpoint

Through the native AiVOOV API, this operation is `GET /voices` (base URL `https://aivoov.com/api/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voices.md) for the provider-specific parameters and requirements.

