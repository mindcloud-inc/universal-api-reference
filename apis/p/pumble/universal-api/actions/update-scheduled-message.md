# Pumble: Update Scheduled Message

Updates an existing scheduled message in Pumble.

```
PUT https://connect.mindcloud.co/v1/universal/pumble/latest/actions/update-scheduled-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pumble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pumble/latest/actions/update-scheduled-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pumble/latest/actions/update-scheduled-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | no |  |
| `scheduledMessageId` | string | no |  |
| `sendAt` | number | no | Unix timestamp in milliseconds for the updated scheduled send time. |
| `text` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "channelId": "string",
      "id": "string",
      "sendAt": 1,
      "text": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `channelId` | string |  |
| `id` | string |  |
| `sendAt` | number |  |
| `text` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Pumble API, this operation is `POST /editScheduledMessage` (base URL `https://pumble-api-keys.addons.marketplace.cake.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-scheduled-message.md) for the provider-specific parameters and requirements.

