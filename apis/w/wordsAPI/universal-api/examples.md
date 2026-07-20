# WordsAPI Universal API Examples

These examples use the MindCloud API key and WordsAPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Word

Retrieves full details for a word from WordsAPI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wordsAPI/latest/actions/get-word?connectionId=$CONNECTION_ID&word=soliloquy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "word": "soliloquy"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wordsAPI/latest/actions/get-word?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Word action reference](actions/get-word.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wordsAPI/latest/actions/get-word).
