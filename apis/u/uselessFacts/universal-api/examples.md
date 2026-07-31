# Useless Facts Universal API Examples

These examples use the MindCloud API key and Useless Facts connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Fetch Random Useless Fact



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uselessFacts/latest/actions/fetch-random-useless-fact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uselessFacts/latest/actions/fetch-random-useless-fact?${params}`, {
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
      "id": "string",
      "language": "string",
      "permalink": "https://example.com",
      "source": "string",
      "source_url": "https://example.com",
      "text": "string"
    }
  ],
  "meta": {}
}
```

See the full [Fetch Random Useless Fact action reference](actions/fetch-random-useless-fact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uselessFacts/latest/actions/fetch-random-useless-fact).
