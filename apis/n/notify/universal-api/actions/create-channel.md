# Notify: Create Channel

Creates a new channel in Notify.

```
POST https://connect.mindcloud.co/v1/universal/notify/latest/actions/create-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/notify/latest/actions/create-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notify/latest/actions/create-channel', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "channel_page": "string",
      "channelId": "string",
      "endpoint": "string",
      "messages": [
        {}
      ],
      "pubKey": "string",
      "time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel_page` | string | The browser subscription page URL for the channel. |
| `channelId` | string | The newly created Notify channel identifier. |
| `endpoint` | string | The channel endpoint URL used to send notifications. |
| `messages` | array<object> | Recent messages on the new channel, usually empty immediately after creation. |
| `pubKey` | string | The VAPID public key used for browser subscriptions. |
| `time` | string | Provider time marker returned by the channel info response. |

## Native endpoint

Through the native Notify API, this operation is `POST /register_channel` (base URL `https://notify.run`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-channel.md) for the provider-specific parameters and requirements.

