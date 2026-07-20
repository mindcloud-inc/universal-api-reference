# Stacker Universal API Examples

These examples use the MindCloud API key and Stacker connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accounts

Retrieves accounts from Stacker.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stacker/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stacker/latest/actions/list-accounts?${params}`, {
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
      "name": "Ava Chen",
      "sid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Accounts action reference](actions/list-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stacker/latest/actions/list-accounts).

## Bulk Create and Update Records

Creates or updates records in a Stacker object.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stacker/latest/actions/bulk-create-and-update-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "objectSid": "string",
  "records[]": [
    {}
  ],
  "stackId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stacker/latest/actions/bulk-create-and-update-records', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "objectSid": "string",
    "records[]": [{}],
    "stackId": "string"
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
      "created": [
        "string"
      ],
      "formatting_errors": [
        {}
      ],
      "updated": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Bulk Create and Update Records action reference](actions/bulk-create-and-update-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stacker/latest/actions/bulk-create-and-update-records).
