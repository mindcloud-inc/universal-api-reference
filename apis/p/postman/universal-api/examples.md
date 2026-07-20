# Postman Universal API Examples

These examples use the MindCloud API key and Postman connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated User

Retrieves authenticated user details and usage limits from Postman.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postman/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postman/latest/actions/get-authenticated-user?${params}`, {
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
      "operations": [
        {
          "limit": 1,
          "name": "Ava Chen",
          "usage": 1
        }
      ],
      "user": {
        "email": "ava@example.com",
        "id": 1,
        "username": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Authenticated User action reference](actions/get-authenticated-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postman/latest/actions/get-authenticated-user).

## Create Environment

Creates a new environment in Postman.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postman/latest/actions/create-environment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "environment.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postman/latest/actions/create-environment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "environment.name": "Ava Chen"
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
      "environment": {
        "id": "string",
        "name": "Ava Chen",
        "uid": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Environment action reference](actions/create-environment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postman/latest/actions/create-environment).
