# Abbreviations Universal API Examples

These examples use the MindCloud API key and Abbreviations connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Lookup Abbreviation



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abbreviations/latest/actions/lookup-abbreviation?connectionId=$CONNECTION_ID&term=asap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "term": "asap"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abbreviations/latest/actions/lookup-abbreviation?${params}`, {
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
      "category": "string",
      "categoryname": "Ava Chen",
      "definition": "string",
      "id": "string",
      "score": "string",
      "term": "string"
    }
  ],
  "meta": {}
}
```

See the full [Lookup Abbreviation action reference](actions/lookup-abbreviation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/abbreviations/latest/actions/lookup-abbreviation).
