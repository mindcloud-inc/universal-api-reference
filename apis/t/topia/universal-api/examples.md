# Topia Universal API Examples

These examples use the MindCloud API key and Topia connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Worlds

Retrieves worlds available to your Topia account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-worlds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-worlds?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "urlSlug": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Worlds action reference](actions/list-worlds.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/topia/latest/actions/list-worlds).
