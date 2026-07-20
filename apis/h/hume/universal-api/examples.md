# Hume Universal API Examples

These examples use the MindCloud API key and Hume connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get chat audio



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hume/latest/actions/get-chat-audio?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hume/latest/actions/get-chat-audio?${params}`, {
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
      "file": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get chat audio action reference](actions/get-chat-audio.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hume/latest/actions/get-chat-audio).

## Create config



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hume/latest/actions/create-config" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "eviVersion": "3",
  "voice": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hume/latest/actions/create-config', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "eviVersion": "3",
    "voice": {}
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
      "createdOn": 1,
      "eviVersion": "string",
      "id": "string",
      "modifiedOn": 1,
      "name": "Ava Chen",
      "prompt": {},
      "tools": [
        [
          {}
        ]
      ],
      "version": 1,
      "versionDescription": "string",
      "voice": {}
    }
  ],
  "meta": {}
}
```

See the full [Create config action reference](actions/create-config.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hume/latest/actions/create-config).
