# Kadoa Universal API Examples

These examples use the MindCloud API key and Kadoa connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Schemas



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/list-schemas?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/list-schemas?${params}`, {
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
      "data": [
        {}
      ],
      "error": true
    }
  ],
  "meta": {}
}
```

See the full [List Schemas action reference](actions/list-schemas.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kadoa/latest/actions/list-schemas).

## Bulk Approve Rules



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/bulk-approve-rules" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ruleIds": "string",
  "workflowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/bulk-approve-rules', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ruleIds": "string",
    "workflowId": "string"
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

See the full [Bulk Approve Rules action reference](actions/bulk-approve-rules.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kadoa/latest/actions/bulk-approve-rules).
