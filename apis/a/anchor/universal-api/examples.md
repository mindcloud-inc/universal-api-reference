# Anchor Universal API Examples

These examples use the MindCloud API key and Anchor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Profiles

Retrieves profiles from Anchor.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anchor/latest/actions/list-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anchor/latest/actions/list-profiles?${params}`, {
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
      "count": 1,
      "items": [
        {
          "created_at": "string",
          "description": "string",
          "name": "Ava Chen",
          "session_id": "string",
          "source": "string",
          "status": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Profiles action reference](actions/list-profiles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/anchor/latest/actions/list-profiles).

## Create Profile

Creates a profile in Anchor.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anchor/latest/actions/create-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anchor/latest/actions/create-profile', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Profile action reference](actions/create-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/anchor/latest/actions/create-profile).
