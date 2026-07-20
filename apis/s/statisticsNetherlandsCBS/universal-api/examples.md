# Statistics Netherlands CBS Universal API Examples

These examples use the MindCloud API key and Statistics Netherlands CBS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Catalog Metadata

Retrieves catalog metadata from Statistics Netherlands CBS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-catalog-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-catalog-metadata?${params}`, {
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
      "rawResponse": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Catalog Metadata action reference](actions/get-catalog-metadata.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/statisticsNetherlandsCBS/latest/actions/get-catalog-metadata).
