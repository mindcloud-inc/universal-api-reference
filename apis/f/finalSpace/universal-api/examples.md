# Final Space Universal API Examples

These examples use the MindCloud API key and Final Space connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Character



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finalSpace/latest/actions/get-character?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finalSpace/latest/actions/get-character?${params}`, {
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
      "abilities": [
        "string"
      ],
      "alias": [
        "string"
      ],
      "gender": "string",
      "id": 1,
      "img_url": "https://example.com",
      "name": "Ava Chen",
      "origin": "string",
      "species": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Character action reference](actions/get-character.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/finalSpace/latest/actions/get-character).
