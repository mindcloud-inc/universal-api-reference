# GSA Public Comment Universal API Examples

These examples use the MindCloud API key and GSA Public Comment connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Agency Categories

Retrieves agency categories for an acronym from GSA Public Comment.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/list-agency-categories?connectionId=$CONNECTION_ID&acronym=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "acronym": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/list-agency-categories?${params}`, {
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
      "data": [
        {
          "attributes": {
            "acronym": "string",
            "category": "string",
            "default": true
          },
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Agency Categories action reference](actions/list-agency-categories.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gSAPublicComment/latest/actions/list-agency-categories).
