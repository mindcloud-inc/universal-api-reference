# BippyBox Universal API Examples

These examples use the MindCloud API key and BippyBox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Data

Retrieves BippyBox account data, devices, colors, and audio files.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bippyBox/latest/actions/get-user-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bippyBox/latest/actions/get-user-data?${params}`, {
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
      "audioFiles": [
        {}
      ],
      "claimedDevices": [
        {}
      ],
      "colors": [
        {}
      ],
      "createdAt": {
        "_nanoseconds": 1,
        "_seconds": 1
      },
      "email": "ava@example.com",
      "firstname": "Ava",
      "isAdmin": true,
      "lastname": "Chen",
      "thingsboardCustomerId": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User Data action reference](actions/get-user-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bippyBox/latest/actions/get-user-data).

## Trigger BippyBox

Triggers a BippyBox device with audio and color.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bippyBox/latest/actions/trigger-bippybox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uid": "string",
  "deviceId": "string",
  "url": "https://example.com",
  "color": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bippyBox/latest/actions/trigger-bippybox', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uid": "string",
    "deviceId": "string",
    "url": "https://example.com",
    "color": "string"
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
      "error": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Trigger BippyBox action reference](actions/trigger-bippybox.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bippyBox/latest/actions/trigger-bippybox).
