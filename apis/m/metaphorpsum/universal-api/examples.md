# Metaphorpsum Universal API Examples

These examples use the MindCloud API key and Metaphorpsum connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Metaphor Paragraphs



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metaphorpsum/latest/actions/get-metaphor-paragraphs?connectionId=$CONNECTION_ID&paragraphCount=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paragraphCount": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metaphorpsum/latest/actions/get-metaphor-paragraphs?${params}`, {
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
      "text": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Metaphor Paragraphs action reference](actions/get-metaphor-paragraphs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/metaphorpsum/latest/actions/get-metaphor-paragraphs).
