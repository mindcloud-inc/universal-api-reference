# Voicemaker: List Voices

Retrieves all available voices from Voicemaker.

```
GET https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/list-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voicemaker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/list-voices?connectionId=$CONNECTION_ID&language=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "language": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/list-voices?${params}`, {
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
| `language` | string | yes | Language code used to filter available voices, for example en-US. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Voicemaker API, this operation is `POST api/v1/voice/list` (base URL `https://developer.voicemaker.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voices.md) for the provider-specific parameters and requirements.

