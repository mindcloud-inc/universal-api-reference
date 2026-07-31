# Rick and Morty Universal API Examples

These examples use the MindCloud API key and Rick and Morty connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Character



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rickAndMorty/latest/actions/get-character?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rickAndMorty/latest/actions/get-character?${params}`, {
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
      "created": "string",
      "episode": [
        "string"
      ],
      "gender": "string",
      "id": 1,
      "image": "string",
      "location": {},
      "name": "Ava Chen",
      "origin": {},
      "species": "string",
      "status": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Character action reference](actions/get-character.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rickAndMorty/latest/actions/get-character).
