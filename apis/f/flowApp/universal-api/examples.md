# Flow App Universal API Examples

These examples use the MindCloud API key and Flow App connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Operators



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/list-operators?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/list-operators?${params}`, {
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
      "accountServiceLevel": 1,
      "accountToken": "string",
      "avatarExtension": "string",
      "avatarToken": "string",
      "bio": "string",
      "company": "string",
      "createdBy": 1,
      "createdDate": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "linkedinUrl": "https://example.com",
      "permission": 1,
      "phone": "string",
      "title": "string",
      "token": "string",
      "twitterID": "string",
      "userID": 1
    }
  ],
  "meta": {}
}
```

See the full [List Operators action reference](actions/list-operators.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flowApp/latest/actions/list-operators).

## Create Event



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "creatorId": 1,
  "title": "string",
  "description": "string",
  "date": "string",
  "time": "string",
  "timezone": "string",
  "operators[]": [
    {}
  ],
  "operators[].id": 1,
  "operators[].role": 1,
  "operators[].micEnabled": true,
  "operators[].camEnabled": true,
  "operators[].screenSharingEnabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "creatorId": 1,
    "title": "string",
    "description": "string",
    "date": "string",
    "time": "string",
    "timezone": "string",
    "operators[]": [{}],
    "operators[].id": 1,
    "operators[].role": 1,
    "operators[].micEnabled": true,
    "operators[].camEnabled": true,
    "operators[].screenSharingEnabled": true
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
      "code": 1,
      "localDescription": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Event action reference](actions/create-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flowApp/latest/actions/create-event).
