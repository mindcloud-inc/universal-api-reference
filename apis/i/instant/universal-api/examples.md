# Instant Universal API Examples

These examples use the MindCloud API key and Instant connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Query Records

Retrieves records from Instant with an InstaQL query.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instant/latest/actions/query-records?connectionId=$CONNECTION_ID&query=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instant/latest/actions/query-records?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Query Records action reference](actions/query-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/instant/latest/actions/query-records).

## Batch Transact Steps

Applies transaction steps to Instant records.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instant/latest/actions/batch-transact-steps" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "steps[]": [
    [
      "string"
    ]
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instant/latest/actions/batch-transact-steps', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "steps[]": [["string"]]
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
      "tx-id": 1
    }
  ],
  "meta": {}
}
```

See the full [Batch Transact Steps action reference](actions/batch-transact-steps.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/instant/latest/actions/batch-transact-steps).
