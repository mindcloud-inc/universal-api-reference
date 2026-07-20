# Pumble: Create Scheduled Message

Creates a scheduled message in Pumble.

```
POST https://connect.mindcloud.co/v1/universal/pumble/latest/actions/create-scheduled-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pumble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pumble/latest/actions/create-scheduled-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pumble/latest/actions/create-scheduled-message', {
  method: 'POST',
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
| `sendAt` | number | no | Unix timestamp in milliseconds for when the message should be sent. |
| `text` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelId": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelId` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Pumble API, this operation is `POST /createScheduledMessage` (base URL `https://pumble-api-keys.addons.marketplace.cake.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-scheduled-message.md) for the provider-specific parameters and requirements.

