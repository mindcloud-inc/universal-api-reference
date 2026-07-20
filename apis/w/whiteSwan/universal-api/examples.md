# White Swan Universal API Examples

These examples use the MindCloud API key and White Swan connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Account Users

Retrieves account users from White Swan.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/list-account-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/list-account-users?${params}`, {
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
      "clients_referred": [
        {}
      ],
      "email": "ava@example.com",
      "name": "Ava Chen",
      "other_partners_referred": [
        {}
      ],
      "permission": "string",
      "total_amount_credited": 1
    }
  ],
  "meta": {}
}
```

See the full [List Account Users action reference](actions/list-account-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whiteSwan/latest/actions/list-account-users).

## Add Case Party

Adds a case party to a White Swan case.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/add-case-party" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "request": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/add-case-party', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "request": "string"
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
      "error_message": "string",
      "request": "string",
      "request_parties": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Case Party action reference](actions/add-case-party.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whiteSwan/latest/actions/add-case-party).
