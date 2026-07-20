# Redbooth Universal API Examples

These examples use the MindCloud API key and Redbooth connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Information

Retrieves the current user's information from Redbooth.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/get-user-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/get-user-information?${params}`, {
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
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen",
      "locale": "string",
      "time_zone": "string",
      "type": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get User Information action reference](actions/get-user-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/redbooth/latest/actions/get-user-information).

## Create Comment

Creates a new comment in Redbooth.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetId": 1,
  "targetType": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetId": 1,
    "targetType": "string",
    "body": "string"
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
      "body": "string",
      "id": 1,
      "project_id": 1,
      "status": "string",
      "target_id": 1,
      "target_type": "string",
      "type": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Comment action reference](actions/create-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/redbooth/latest/actions/create-comment).
