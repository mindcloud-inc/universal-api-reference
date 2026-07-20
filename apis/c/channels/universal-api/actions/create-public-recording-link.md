# Channels: Create Public Recording Link

Creates a public recording link in Channels.

```
POST https://connect.mindcloud.co/v1/universal/channels/latest/actions/create-public-recording-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/channels/latest/actions/create-public-recording-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "callId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channels/latest/actions/create-public-recording-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "callId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callId` | number | yes | Call ID that belongs to the recording. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callId": 1,
      "link": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callId` | number |  |
| `link` | string |  |

## Native endpoint

Through the native Channels API, this operation is `POST /api/v1/recordings` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-public-recording-link.md) for the provider-specific parameters and requirements.

