# Airzone Cloud Universal API Examples

These examples use the MindCloud API key and Airzone Cloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user profile from Airzone Cloud.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-current-user?${params}`, {
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
      "_id": "string",
      "config": {},
      "confirmation_date": "string",
      "created_at": "string",
      "data": {},
      "email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airzoneCloud/latest/actions/get-current-user).

## Create Session Token Pair

Creates a session token pair in Airzone Cloud.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/create-session-token-pair" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/create-session-token-pair', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "password": "string"
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
      "_id": "string",
      "config": {},
      "confirmation_date": "string",
      "created_at": "string",
      "data": {},
      "email": "ava@example.com",
      "migrated": true,
      "pendingMigration": true,
      "refreshToken": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Session Token Pair action reference](actions/create-session-token-pair.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airzoneCloud/latest/actions/create-session-token-pair).
