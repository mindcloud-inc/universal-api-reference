# EZICHEQ Universal API Examples

These examples use the MindCloud API key and EZICHEQ connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test Connection

Tests your EZICHEQ connection.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eZICHEQ/latest/actions/test-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eZICHEQ/latest/actions/test-connection?${params}`, {
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

See the full [Test Connection action reference](actions/test-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eZICHEQ/latest/actions/test-connection).

## Create Item

Creates an item in EZICHEQ.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eZICHEQ/latest/actions/create-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "item.itemTypeId": "string",
  "item.labelNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eZICHEQ/latest/actions/create-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "item.itemTypeId": "string",
    "item.labelNumber": "string"
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
      "count": 1,
      "date": "string",
      "error": "string",
      "request_method": "string",
      "request_uri": "string",
      "results": {},
      "status": "string",
      "status_code": 1,
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Item action reference](actions/create-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eZICHEQ/latest/actions/create-item).
