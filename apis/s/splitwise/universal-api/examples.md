# Splitwise Universal API Examples

These examples use the MindCloud API key and Splitwise connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user's details from Splitwise.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/get-current-user?${params}`, {
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
      "addFriendUrl": "https://example.com",
      "countryCode": "string",
      "customPicture": true,
      "dateFormat": "string",
      "defaultCurrency": "string",
      "defaultGroupId": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "forceRefreshAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "lastName": "Chen",
      "locale": "string",
      "notifications": {},
      "notificationsCount": 1,
      "notificationsRead": "2026-05-07T12:00:00.000Z",
      "picture": {},
      "registrationStatus": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/splitwise/latest/actions/get-current-user).

## Create Comment

Creates a new expense comment in Splitwise.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "expenseId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "expenseId": 1
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
      "comment": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Comment action reference](actions/create-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/splitwise/latest/actions/create-comment).
