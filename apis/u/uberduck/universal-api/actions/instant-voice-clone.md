# Uberduck: Instant Voice Clone

Creates a zero-shot voice in Uberduck.

```
POST https://connect.mindcloud.co/v1/universal/uberduck/latest/actions/instant-voice-clone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uberduck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uberduck/latest/actions/instant-voice-clone" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "paths": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uberduck/latest/actions/instant-voice-clone', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "paths": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name for the new zero-shot voice clone. |
| `paths` | list<string> | yes | List of source audio URLs Uberduck should use for cloning. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "displayName": "Ava Chen",
      "isPrivate": true,
      "name": "Ava Chen",
      "sampleUrl": "https://example.com",
      "tags": [
        "string"
      ],
      "voicemodelUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `displayName` | string |  |
| `isPrivate` | boolean |  |
| `name` | string |  |
| `sampleUrl` | string |  |
| `tags` | array<string> |  |
| `voicemodelUuid` | string |  |

## Native endpoint

Through the native Uberduck API, this operation is `POST /v1/voices` (base URL `https://api.uberduck.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/instant-voice-clone.md) for the provider-specific parameters and requirements.

