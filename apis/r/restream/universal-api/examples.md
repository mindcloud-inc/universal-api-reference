# Restream Universal API Examples

These examples use the MindCloud API key and Restream connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Profile

Retrieves the authenticated user profile from Restream.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-profile?${params}`, {
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
      "email": "ava@example.com",
      "id": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Profile action reference](actions/get-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/restream/latest/actions/get-profile).

## Add Channel

Creates a streaming channel in Restream.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/restream/latest/actions/add-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "platformId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/restream/latest/actions/add-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "platformId": 1
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
      "channelUrl": "https://example.com",
      "displayName": "Ava Chen",
      "id": 1,
      "platformId": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Channel action reference](actions/add-channel.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/restream/latest/actions/add-channel).
