# Unbounce Universal API Examples

These examples use the MindCloud API key and Unbounce connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accounts

Retrieves the accounts collection from Unbounce.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/list-accounts?${params}`, {
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
      "accounts": [
        {}
      ],
      "metadata": {}
    }
  ],
  "meta": {}
}
```

See the full [List Accounts action reference](actions/list-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/unbounce/latest/actions/list-accounts).

## Create Lead Deletion Request

Creates an asynchronous lead deletion request in Unbounce.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/create-lead-deletion-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "page_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/create-lead-deletion-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "page_id": "string"
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
      "completedAt": "string",
      "createdAt": "string",
      "createdBy": "string",
      "id": "string",
      "metadata": {},
      "pageId": "string",
      "query": {},
      "status": "string",
      "totalLeadsDeleted": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Lead Deletion Request action reference](actions/create-lead-deletion-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/unbounce/latest/actions/create-lead-deletion-request).
