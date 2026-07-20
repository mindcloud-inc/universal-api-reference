# Voicemaker: List Voice Clones

Retrieves all voice clones from Voicemaker.

```
GET https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/list-voice-clones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voicemaker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/list-voice-clones?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/list-voice-clones?${params}`, {
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
| `page` | number | no | Page number to return. |
| `limit` | number | no | Maximum number of voice clones to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clonesLimit": 1,
      "count": 1,
      "data": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clonesLimit` | number |  |
| `count` | number |  |
| `data` | array<object> |  |
| `success` | boolean |  |

## Native endpoint

Through the native Voicemaker API, this operation is `GET api/v1/voice-clones` (base URL `https://developer.voicemaker.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voice-clones.md) for the provider-specific parameters and requirements.

