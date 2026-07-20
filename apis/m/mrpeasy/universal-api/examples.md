# MRPeasy Universal API Examples

These examples use the MindCloud API key and MRPeasy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves customers from MRPeasy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/list-customers?${params}`, {
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
      "code": "string",
      "contactData": [
        "string"
      ],
      "created": "string",
      "customerId": 1,
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mrpeasy/latest/actions/list-customers).

## Create BOM

Creates a new BOM in MRPeasy.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/create-bom" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": 1,
  "title": "string",
  "components": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/create-bom', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": 1,
    "title": "string",
    "components": [{}]
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

See the full [Create BOM action reference](actions/create-bom.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mrpeasy/latest/actions/create-bom).
