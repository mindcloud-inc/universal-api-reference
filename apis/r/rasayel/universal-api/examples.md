# Rasayel Universal API Examples

These examples use the MindCloud API key and Rasayel connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get App

Retrieves the current Rasayel workspace details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/get-app?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/get-app?${params}`, {
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
      "companyDomain": "string",
      "createdAt": 1,
      "displayName": "Ava Chen",
      "id": 1,
      "updatedAt": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get App action reference](actions/get-app.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rasayel/latest/actions/get-app).

## Assign Conversation

Assigns a conversation to a user in Rasayel.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/assign-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/assign-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "clientMutationId": "string",
      "message": {}
    }
  ],
  "meta": {}
}
```

See the full [Assign Conversation action reference](actions/assign-conversation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rasayel/latest/actions/assign-conversation).
