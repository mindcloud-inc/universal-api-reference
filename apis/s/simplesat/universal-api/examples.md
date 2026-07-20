# Simplesat Universal API Examples

These examples use the MindCloud API key and Simplesat connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Surveys

Retrieves surveys from Simplesat.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/list-surveys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/list-surveys?${params}`, {
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
      "brand_name": "Ava Chen",
      "id": 1,
      "metric": "string",
      "name": "Ava Chen",
      "survey_token": "string",
      "survey_type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Surveys action reference](actions/list-surveys.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simplesat/latest/actions/list-surveys).

## Bulk Upsert Customers

Creates or updates multiple customers in Simplesat.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/bulk-upsert-customers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/bulk-upsert-customers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "detail": "string",
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Bulk Upsert Customers action reference](actions/bulk-upsert-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simplesat/latest/actions/bulk-upsert-customers).
