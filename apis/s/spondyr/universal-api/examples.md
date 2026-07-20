# Spondyr Universal API Examples

These examples use the MindCloud API key and Spondyr connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Transaction Types

Retrieves transaction types from Spondyr.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/list-transaction-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/list-transaction-types?${params}`, {
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
      "APIStatus": "string",
      "Data": [
        {}
      ],
      "ErrorMessage": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Transaction Types action reference](actions/list-transaction-types.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/spondyr/latest/actions/list-transaction-types).

## Create Condition

Creates a new condition for a transaction type in Spondyr.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/create-condition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionType": "string",
  "name": "Ava Chen",
  "fieldName": "Ava Chen",
  "possibleValues": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/create-condition', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionType": "string",
    "name": "Ava Chen",
    "fieldName": "Ava Chen",
    "possibleValues": "string"
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
      "APIStatus": "string",
      "ErrorMessage": "string",
      "ReferenceID": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Condition action reference](actions/create-condition.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/spondyr/latest/actions/create-condition).
