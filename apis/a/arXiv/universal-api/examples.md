# arXiv Universal API Examples

These examples use the MindCloud API key and arXiv connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Papers

Finds papers in arXiv by search query.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/search-papers?connectionId=$CONNECTION_ID&limit=25&offset=0&searchQuery=all%3Atransformer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "searchQuery": "all:transformer"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/arXiv/latest/actions/search-papers?${params}`, {
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
      "arxiv:comment": "string",
      "arxiv:primary_category": {},
      "author": [
        {}
      ],
      "category": [
        {}
      ],
      "id": "string",
      "published": "2026-05-07T12:00:00.000Z",
      "summary": "string",
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Search Papers action reference](actions/search-papers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/arXiv/latest/actions/search-papers).
