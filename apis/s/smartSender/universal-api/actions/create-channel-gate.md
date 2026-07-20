# Smart Sender: Create Channel Gate

Creates a channel gateway in Smart Sender, or returns the existing one.

```
POST https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/create-channel-gate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smart Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/create-channel-gate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/create-channel-gate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "identifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | The Smart Sender channel ID. |
| `firstName` | string | no | First name for the created gateway contact. |
| `identifier` | string | yes | Messenger identifier for the contact gateway. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": {},
      "contact": {},
      "id": 1,
      "subscribed": true,
      "unreadMessages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | object |  |
| `contact` | object |  |
| `id` | number |  |
| `subscribed` | boolean |  |
| `unreadMessages` | number |  |

## Native endpoint

Through the native Smart Sender API, this operation is `POST /v1/channels/:channelId/gates` (base URL `https://api.smartsender.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-channel-gate.md) for the provider-specific parameters and requirements.

