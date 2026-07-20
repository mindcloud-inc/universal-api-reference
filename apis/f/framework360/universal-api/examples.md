# Framework360 Universal API Examples

These examples use the MindCloud API key and Framework360 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Profile



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/framework360/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/framework360/latest/actions/get-user-profile?${params}`, {
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
      "active": 1,
      "avatar": "string",
      "cognome": "string",
      "email": "ava@example.com",
      "formatted_name": "Ava Chen",
      "has_wizard": 1,
      "id": "string",
      "nome": "string",
      "ruolo": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User Profile action reference](actions/get-user-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/framework360/latest/actions/get-user-profile).

## Create Chat



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/framework360/latest/actions/chat-create" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/framework360/latest/actions/chat-create', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "message": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create Chat action reference](actions/chat-create.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/framework360/latest/actions/chat-create).
