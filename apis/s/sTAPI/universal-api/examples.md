# STAPI Universal API Examples

These examples use the MindCloud API key and STAPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Character



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/get-character?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/get-character?${params}`, {
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
      "character": {
        "deceased": true,
        "gender": "string",
        "hologram": true,
        "name": "Ava Chen",
        "uid": "string",
        "yearOfBirth": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Character action reference](actions/get-character.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sTAPI/latest/actions/get-character).
