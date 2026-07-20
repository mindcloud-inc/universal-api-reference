# NetSuite - Basic Universal API Examples

These examples use the MindCloud API key and NetSuite - Basic connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accounts

Retrieves a list of accounts from NetSuite.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/list-accounts?${params}`, {
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
      "__meta": {
        "presentation": {
          "entityUrl": "https://example.com",
          "fields": {
            "id": "string",
            "name": "Ava Chen"
          },
          "type": "string"
        }
      },
      "id": "string",
      "links": [
        {
          "href": "https://example.com",
          "method": "https://example.com",
          "rel": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Accounts action reference](actions/list-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/netSuiteBasic/latest/actions/list-accounts).

## Create Account

Creates a new account in NetSuite.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/create-account', {
  method: 'POST',
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
  "data": [],
  "meta": {}
}
```

See the full [Create Account action reference](actions/create-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/netSuiteBasic/latest/actions/create-account).
