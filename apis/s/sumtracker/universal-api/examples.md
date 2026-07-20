# Sumtracker Universal API Examples

These examples use the MindCloud API key and Sumtracker connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Warehouses

Retrieves warehouses from Sumtracker.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-warehouses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-warehouses?${params}`, {
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
      "code": "string",
      "priority": 1,
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [List Warehouses action reference](actions/list-warehouses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sumtracker/latest/actions/list-warehouses).

## Create Goods Receipt Note

Creates a goods receipt note in Sumtracker.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/create-grn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document_type": "string",
  "po_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/create-grn', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document_type": "string",
    "po_id": "string"
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

See the full [Create Goods Receipt Note action reference](actions/create-grn.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sumtracker/latest/actions/create-grn).
