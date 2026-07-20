# NextBrain Universal API Examples

These examples use the MindCloud API key and NextBrain connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Retrieves available model IDs from NextBrain.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextBrain/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextBrain/latest/actions/list-models?${params}`, {
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

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nextBrain/latest/actions/list-models).

## Import Matrix Data

Imports matrix data into a NextBrain dataset.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nextBrain/latest/actions/import-matrix-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "matrix[]": [
    [
      "string"
    ]
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextBrain/latest/actions/import-matrix-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "matrix[]": [["string"]]
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

See the full [Import Matrix Data action reference](actions/import-matrix-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nextBrain/latest/actions/import-matrix-data).
