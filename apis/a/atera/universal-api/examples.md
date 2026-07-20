# Atera Universal API Examples

These examples use the MindCloud API key and Atera connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get account info

Retrieves account details from Atera.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atera/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atera/latest/actions/get-account-info?${params}`, {
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
      "accountID": "string",
      "companyName": "Ava Chen",
      "country": "string",
      "createdOn": "string",
      "isITDepartment": true,
      "plan": "string",
      "timeZoneName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get account info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/atera/latest/actions/get-account-info).

## Add ticket comment

Creates a comment on a specific Atera ticket.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atera/latest/actions/add-ticket-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": 1,
  "commentText": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atera/latest/actions/add-ticket-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": 1,
    "commentText": "string"
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
      "ActionID": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add ticket comment action reference](actions/add-ticket-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/atera/latest/actions/add-ticket-comment).
