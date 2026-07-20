# DataForSEO Universal API Examples

These examples use the MindCloud API key and DataForSEO connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Bulk Keyword Difficulty

Retrieves bulk keyword difficulty from DataForSEO.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-bulk-keyword-difficulty?connectionId=$CONNECTION_ID&keywords%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keywords[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-bulk-keyword-difficulty?${params}`, {
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
      "keyword": "string",
      "keywordDifficulty": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Bulk Keyword Difficulty action reference](actions/get-bulk-keyword-difficulty.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataForSEO/latest/actions/get-bulk-keyword-difficulty).
