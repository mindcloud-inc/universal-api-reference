# D&D 5e Universal API Examples

These examples use the MindCloud API key and D&D 5e connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Class



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dD5e/latest/actions/get-classe?connectionId=$CONNECTION_ID&index=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "index": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dD5e/latest/actions/get-classe?${params}`, {
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
      "desc": [
        "string"
      ],
      "index": "string",
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Class action reference](actions/get-classe.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dD5e/latest/actions/get-classe).
