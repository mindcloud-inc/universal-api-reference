# ChartMogul Universal API Examples

These examples use the MindCloud API key and ChartMogul connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves customers from ChartMogul.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-customers?${params}`, {
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
      "arr": 1,
      "city": "string",
      "company": "string",
      "country": "string",
      "currency": "string",
      "customerSince": "2026-05-07T12:00:00.000Z",
      "dataSourceUuid": "string",
      "email": "ava@example.com",
      "externalId": "string",
      "id": 1,
      "lastSeen": "2026-05-07T12:00:00.000Z",
      "mrr": 1,
      "name": "Ava Chen",
      "state": "string",
      "status": "string",
      "uuid": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chartMogul/latest/actions/list-customers).
