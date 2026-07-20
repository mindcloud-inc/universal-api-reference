# Notify: Get Current Channel Info

Retrieves current channel details from Notify.

```
GET https://connect.mindcloud.co/v1/universal/notify/latest/actions/get-current-channel-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notify/latest/actions/get-current-channel-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notify/latest/actions/get-current-channel-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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
| `channelId` | string | The Notify channel identifier. |
| `endpoint` | string | The channel endpoint URL used to send notifications. |
| `messages` | array<object> | The most recent messages for the channel. |
| `pubKey` | string | The VAPID public key used for browser subscriptions. |
| `time` | string | Provider time marker returned by the channel info response. |

## Native endpoint

Through the native Notify API, this operation is `GET /{{credentials.channelToken}}/json` (base URL `https://notify.run`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-channel-info.md) for the provider-specific parameters and requirements.

