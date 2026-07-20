# Prospeo Universal API Examples

These examples use the MindCloud API key and Prospeo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Bulk Enrich Companies

Retrieves enriched company data from Prospeo in bulk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/bulk-enrich-companies?connectionId=$CONNECTION_ID&data%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/bulk-enrich-companies?${params}`, {
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
      "invalidDatapoints": [
        {}
      ],
      "matched": [
        {}
      ],
      "notMatched": [
        {}
      ],
      "totalCost": 1
    }
  ],
  "meta": {}
}
```

See the full [Bulk Enrich Companies action reference](actions/bulk-enrich-companies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/prospeo/latest/actions/bulk-enrich-companies).
