# Talk Python To Me Universal API Examples

These examples use the MindCloud API key and Talk Python To Me connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Episodes and Transcripts

Finds episodes and transcripts in Talk Python To Me.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talkPythonToMe/latest/actions/search-episodes-and-transcripts?connectionId=$CONNECTION_ID&query=python-testing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "python-testing"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talkPythonToMe/latest/actions/search-episodes-and-transcripts?${params}`, {
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
      "description": "string",
      "id": 1,
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Search Episodes and Transcripts action reference](actions/search-episodes-and-transcripts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/talkPythonToMe/latest/actions/search-episodes-and-transcripts).
