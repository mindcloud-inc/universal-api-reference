# Veracity Learning Universal API Examples

These examples use the MindCloud API key and Veracity Learning connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Statements

Retrieves statements from Veracity Learning.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/list-statements?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/list-statements?${params}`, {
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
      "actor": {},
      "authority": {},
      "context": {},
      "id": "string",
      "object": {},
      "result": {},
      "stored": "2026-05-07T12:00:00.000Z",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "verb": {}
    }
  ],
  "meta": {}
}
```

See the full [List Statements action reference](actions/list-statements.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/veracityLearning/latest/actions/list-statements).

## Create Statements

Creates one or more statements in Veracity Learning.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/create-statements" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "statements[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/create-statements', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "statements[]": [{}]
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
      "statementId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Statements action reference](actions/create-statements.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/veracityLearning/latest/actions/create-statements).
