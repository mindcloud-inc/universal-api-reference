# Urban Dictionary Universal API Examples

These examples use the MindCloud API key and Urban Dictionary connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Look Up Definitions



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/urbanDictionary/latest/actions/look-up-definitions?connectionId=$CONNECTION_ID&term=e.g.%2C%20yeet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "term": "e.g., yeet"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/urbanDictionary/latest/actions/look-up-definitions?${params}`, {
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
      "author": "string",
      "current_vote": "string",
      "defid": 1,
      "definition": "string",
      "example": "string",
      "permalink": "https://example.com",
      "sound_urls": [
        "https://example.com"
      ],
      "thumbs_down": 1,
      "thumbs_up": 1,
      "word": "string",
      "written_on": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Look Up Definitions action reference](actions/look-up-definitions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/urbanDictionary/latest/actions/look-up-definitions).
