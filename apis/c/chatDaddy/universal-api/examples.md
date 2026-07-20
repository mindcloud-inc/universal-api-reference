# ChatDaddy Universal API Examples

These examples use the MindCloud API key and ChatDaddy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves contact records from your ChatDaddy account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/list-contacts?${params}`, {
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
      "contacts": [
        {}
      ],
      "nextPage": "string",
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatDaddy/latest/actions/list-contacts).

## Close Account Connection

Closes a connection to a ChatDaddy account.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/close-account-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "acc_9d2c3b61-174e-42c5-be_0804"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/close-account-connection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "acc_9d2c3b61-174e-42c5-be_0804"
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
      "closing": true,
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Close Account Connection action reference](actions/close-account-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatDaddy/latest/actions/close-account-connection).
