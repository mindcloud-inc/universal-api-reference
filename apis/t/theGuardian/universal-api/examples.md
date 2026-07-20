# The Guardian Universal API Examples

These examples use the MindCloud API key and The Guardian connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Editions

Finds matching editions in The Guardian.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/list-editions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/list-editions?${params}`, {
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
      "apiUrl": "https://example.com",
      "edition": "string",
      "id": "string",
      "path": "string",
      "webTitle": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Editions action reference](actions/list-editions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/theGuardian/latest/actions/list-editions).
