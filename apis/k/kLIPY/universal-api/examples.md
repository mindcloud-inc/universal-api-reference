# KLIPY Universal API Examples

These examples use the MindCloud API key and KLIPY connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List GIF Categories

Retrieves available GIF categories from KLIPY.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kLIPY/latest/actions/list-gif-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kLIPY/latest/actions/list-gif-categories?${params}`, {
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

See the full [List GIF Categories action reference](actions/list-gif-categories.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kLIPY/latest/actions/list-gif-categories).
