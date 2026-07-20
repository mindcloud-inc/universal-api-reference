# Powrbot Universal API Examples

These examples use the MindCloud API key and Powrbot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Company

Finds a company in Powrbot by company name.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powrbot/latest/actions/search-company?connectionId=$CONNECTION_ID&company=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "company": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powrbot/latest/actions/search-company?${params}`, {
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
      "search:display_url": "https://example.com",
      "search:snippet": "string",
      "wiki:Industry": [
        "string"
      ],
      "wiki:Website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Search Company action reference](actions/search-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/powrbot/latest/actions/search-company).

## Start Bulk Search

Creates a bulk search job in Powrbot.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/powrbot/latest/actions/start-bulk-search" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "csv_file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/powrbot/latest/actions/start-bulk-search', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "csv_file": "string"
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
      "company_count": 1,
      "count": 1,
      "count_completed": 1,
      "id": 1,
      "is_completed": true,
      "search_type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Start Bulk Search action reference](actions/start-bulk-search.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/powrbot/latest/actions/start-bulk-search).
