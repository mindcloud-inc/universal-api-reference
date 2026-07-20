# OpenThesaurus Universal API Examples

These examples use the MindCloud API key and OpenThesaurus connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Synonyms



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openThesaurus/latest/actions/search-synonyms?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openThesaurus/latest/actions/search-synonyms?${params}`, {
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
      "id": 1,
      "terms": [
        {
          "level": "string",
          "term": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Search Synonyms action reference](actions/search-synonyms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openThesaurus/latest/actions/search-synonyms).
