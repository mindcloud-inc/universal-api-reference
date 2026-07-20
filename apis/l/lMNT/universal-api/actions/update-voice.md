# LMNT: Update Voice

Updates an existing voice in LMNT.

```
PUT https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/update-voice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LMNT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/update-voice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/update-voice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional updated description for the voice. |
| `gender` | string | no | Optional updated gender tag for the voice. |
| `id` | string | yes | The id of the voice. |
| `name` | string | no | Optional updated display name for the voice. |
| `starred` | boolean | no | When true, adds the voice to your starred list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "voice": {
        "gender": "string",
        "id": "string",
        "name": "Ava Chen",
        "owner": "string",
        "preview_url": "https://example.com",
        "starred": true,
        "state": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `voice` | object |  |
| `voice.gender` | string |  |
| `voice.id` | string |  |
| `voice.name` | string |  |
| `voice.owner` | string |  |
| `voice.preview_url` | string |  |
| `voice.starred` | boolean |  |
| `voice.state` | string |  |
| `voice.type` | string |  |

## Native endpoint

Through the native LMNT API, this operation is `PUT /v1/ai/voice/:id` (base URL `https://api.lmnt.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-voice.md) for the provider-specific parameters and requirements.

