# Opinion Stage Universal API Examples

These examples use the MindCloud API key and Opinion Stage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Items

Retrieves a list of items from Opinion Stage.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/opinionStage/latest/actions/list-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/opinionStage/latest/actions/list-items?${params}`, {
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
      "attributes": {
        "embed": {
          "iframe": "string",
          "script": "string"
        },
        "status": "string",
        "timestamps": {
          "created": "2026-05-07T12:00:00.000Z",
          "modified": "2026-05-07T12:00:00.000Z"
        },
        "title": "string"
      },
      "id": "string",
      "links": {
        "edit": "https://example.com",
        "iframe": "https://example.com",
        "landing": "https://example.com",
        "results": "https://example.com",
        "self": "https://example.com"
      },
      "relationships": {
        "questions": {
          "links": {
            "related": "https://example.com"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Items action reference](actions/list-items.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/opinionStage/latest/actions/list-items).
