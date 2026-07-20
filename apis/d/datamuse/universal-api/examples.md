# Datamuse Universal API Examples

These examples use the MindCloud API key and Datamuse connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Find Adjectives For Noun

Finds adjectives that often describe a noun in Datamuse.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-adjectives-for-noun?connectionId=$CONNECTION_ID&noun=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "noun": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-adjectives-for-noun?${params}`, {
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
      "score": 1,
      "word": "string"
    }
  ],
  "meta": {}
}
```

See the full [Find Adjectives For Noun action reference](actions/find-adjectives-for-noun.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/datamuse/latest/actions/find-adjectives-for-noun).
