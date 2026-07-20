# Anyware Services Universal API Examples

These examples use the MindCloud API key and Anyware Services connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Import Content At Root

Creates a page and imported content at the site root in Anyware Services.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anywareServices/latest/actions/import-content-at-root" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "site": "string",
  "lang": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anywareServices/latest/actions/import-content-at-root', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "site": "string",
    "lang": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "errors": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Import Content At Root action reference](actions/import-content-at-root.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/anywareServices/latest/actions/import-content-at-root).
