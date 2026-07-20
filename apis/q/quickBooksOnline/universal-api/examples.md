# QuickBooks Online Universal API Examples

These examples use the MindCloud API key and QuickBooks Online connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-customers?${params}`, {
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
      "active": true,
      "balance": 1,
      "companyName": "Ava Chen",
      "currencyRef": {},
      "displayName": "Ava Chen",
      "fullyQualifiedName": "Ava Chen",
      "id": "string",
      "metaData": {},
      "primaryEmailAddr": {},
      "syncToken": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quickBooksOnline/latest/actions/list-customers).

## Create Account



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Office Supplies",
  "accountType": "Expense"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Office Supplies",
    "accountType": "Expense"
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
      "accountSubType": "string",
      "accountType": "string",
      "active": true,
      "classification": "string",
      "currentBalance": 1,
      "fullyQualifiedName": "Ava Chen",
      "id": "string",
      "metaData": {},
      "name": "Ava Chen",
      "syncToken": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Account action reference](actions/create-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quickBooksOnline/latest/actions/create-account).
