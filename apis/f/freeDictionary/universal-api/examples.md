# Free Dictionary Universal API Examples

These examples use the MindCloud API key and Free Dictionary connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Word Entries



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freeDictionary/latest/actions/get-word-entries?connectionId=$CONNECTION_ID&language=string&word=example%3A%20hello" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "language": "string",
  "word": "example: hello"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freeDictionary/latest/actions/get-word-entries?${params}`, {
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
      "license": {},
      "meanings": [
        {}
      ],
      "origin": "string",
      "phonetic": "string",
      "phonetics": [
        {}
      ],
      "sourceUrls": [
        "https://example.com"
      ],
      "word": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Word Entries action reference](actions/get-word-entries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freeDictionary/latest/actions/get-word-entries).
