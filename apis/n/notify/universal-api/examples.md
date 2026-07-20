# Notify Universal API Examples

These examples use the MindCloud API key and Notify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Channel Info

Retrieves current channel details from Notify.

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

Example response:

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

See the full [Get Current Channel Info action reference](actions/get-current-channel-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/notify/latest/actions/get-current-channel-info).

## Create Channel

Creates a new channel in Notify.

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

Example response:

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

See the full [Create Channel action reference](actions/create-channel.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/notify/latest/actions/create-channel).
