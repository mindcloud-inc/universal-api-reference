# Blueink: Create Embedded Signing URL

Creates an embedded signing URL for a Blueink packet.

```
POST https://connect.mindcloud.co/v1/universal/blueink/latest/actions/create-embedded-signing-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blueink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blueink/latest/actions/create-embedded-signing-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueink/latest/actions/create-embedded-signing-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "packetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `packetId` | string | yes | Packet ID to generate an embedded signing URL for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expires": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Blueink API, this operation is `POST /packets/:packetId/embed_url/` (base URL `https://api.blueink.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-embedded-signing-url.md) for the provider-specific parameters and requirements.

