# Catalog Machine Universal API Examples

These examples use the MindCloud API key and Catalog Machine connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products

Retrieves all products from Catalog Machine.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/catalogMachine/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/catalogMachine/latest/actions/list-products?${params}`, {
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
      "products": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/catalogMachine/latest/actions/list-products).

## Import CSV Content

Starts a CSV import job in Catalog Machine.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/catalogMachine/latest/actions/import-csv-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "csv": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/catalogMachine/latest/actions/import-csv-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "csv": "string"
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
      "Errors": [
        {}
      ],
      "JobId": "string",
      "RecordsCount": 1,
      "Success": true
    }
  ],
  "meta": {}
}
```

See the full [Import CSV Content action reference](actions/import-csv-content.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/catalogMachine/latest/actions/import-csv-content).
