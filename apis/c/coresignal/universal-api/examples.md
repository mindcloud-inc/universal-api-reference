# Coresignal Universal API Examples

These examples use the MindCloud API key and Coresignal connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Collect Base Company By ID

Collects a base company from Coresignal by ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-base-company-by-id?connectionId=$CONNECTION_ID&companyId=95737800" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "95737800"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-base-company-by-id?${params}`, {
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
      "canonical_url": "https://example.com",
      "employees_count": 1,
      "headquarters_country_parsed": "string",
      "id": 1,
      "industry": "string",
      "name": "Ava Chen",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Collect Base Company By ID action reference](actions/collect-base-company-by-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/coresignal/latest/actions/collect-base-company-by-id).

## Bulk Collect Base Companies By DSL

Creates a bulk base company DSL collection request in Coresignal.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/bulk-collect-base-companies-by-dsl" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "esDslQuery": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/bulk-collect-base-companies-by-dsl', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "esDslQuery": "[object Object]"
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
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Bulk Collect Base Companies By DSL action reference](actions/bulk-collect-base-companies-by-dsl.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/coresignal/latest/actions/bulk-collect-base-companies-by-dsl).
