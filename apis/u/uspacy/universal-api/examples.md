# Uspacy Universal API Examples

These examples use the MindCloud API key and Uspacy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Self Profile

Retrieves the authenticated user profile from Uspacy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/get-self-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/get-self-profile?${params}`, {
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
      "active": true,
      "firstName": "Ava",
      "id": 1,
      "isOnline": true,
      "lastName": "Chen",
      "lastSeenAt": "2026-05-07T12:00:00.000Z",
      "registered": true
    }
  ],
  "meta": {}
}
```

See the full [Get Self Profile action reference](actions/get-self-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uspacy/latest/actions/get-self-profile).

## Create Activity

Creates a new activity in Uspacy.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "start_time": 1,
  "end_time": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "start_time": 1,
    "end_time": 1
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
      "created_at": 1,
      "end_time": 1,
      "id": 1,
      "priority": "string",
      "responsible_id": 1,
      "start_time": 1,
      "status": "string",
      "title": "string",
      "type": "string",
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Activity action reference](actions/create-activity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uspacy/latest/actions/create-activity).
