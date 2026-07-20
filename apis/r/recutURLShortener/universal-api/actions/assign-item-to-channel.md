# Recut URL Shortener: Assign Item To Channel

Assigns an item to a channel in Recut URL Shortener.

```
POST https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/assign-item-to-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/assign-item-to-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelid": 1,
  "type": "links",
  "itemid": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/assign-item-to-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelid": 1,
    "type": "links",
    "itemid": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelid` | number | yes | Channel ID. |
| `type` | string | yes | Item type: `links`, `bio`, or `qr`. Example: `links`. |
| `itemid` | number | yes | Item ID. |

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
| `error` | number | Recut API error flag. |
| `message` | string | Assignment result message. |

## Native endpoint

Through the native Recut URL Shortener API, this operation is `POST /channel/:channelid/assign/:type/:itemid` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-item-to-channel.md) for the provider-specific parameters and requirements.

