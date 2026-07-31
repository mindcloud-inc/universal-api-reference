# Evil Insult Universal API Examples

These examples use the MindCloud API key and Evil Insult connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate Insult (JSON)



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evilInsult/latest/actions/generate-insult-json?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evilInsult/latest/actions/generate-insult-json?${params}`, {
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
      "active": "string",
      "comment": "string",
      "created": "string",
      "createdby": "string",
      "insult": "string",
      "language": "string",
      "number": "string",
      "shown": "string"
    }
  ],
  "meta": {}
}
```

See the full [Generate Insult (JSON) action reference](actions/generate-insult-json.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/evilInsult/latest/actions/generate-insult-json).
