# Hyperise Universal API Examples

These examples use the MindCloud API key and Hyperise connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Hyperise.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/get-current-user?${params}`, {
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
      "createdAt": "string",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hyperise/latest/actions/get-current-user).

## Create Business

Creates a new business in Hyperise.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/create-business" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessName": "Ava Chen",
  "email": "ava@example.com",
  "website": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/create-business', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessName": "Ava Chen",
    "email": "ava@example.com",
    "website": "string"
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
      "businessName": "Ava Chen",
      "createdAt": "string",
      "email": "ava@example.com",
      "id": 1,
      "updatedAt": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Business action reference](actions/create-business.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hyperise/latest/actions/create-business).
