# JmpTo: Assign Item to Channel

Assigns an item to a channel in JmpTo.

```
PUT https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/assign-item-to-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/assign-item-to-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": 1,
  "type": "string",
  "itemId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/assign-item-to-channel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": 1,
    "type": "string",
    "itemId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | number | yes | Channel ID to assign the item to. |
| `type` | string | yes | Item type to assign to the channel. |
| `itemId` | number | yes | Item ID to assign to the channel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | number | Provider success/error code. |
| `message` | string | Assignment result message. |

## Native endpoint

Through the native JmpTo API, this operation is `POST /channel/:channelid/assign/:type/:itemid` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-item-to-channel.md) for the provider-specific parameters and requirements.

