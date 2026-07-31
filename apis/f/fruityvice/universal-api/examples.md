# Fruityvice Universal API Examples

These examples use the MindCloud API key and Fruityvice connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get fruit by ID



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fruityvice/latest/actions/get-fruit-by-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fruityvice/latest/actions/get-fruit-by-id?${params}`, {
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
      "family": "string",
      "genus": "string",
      "id": 1,
      "name": "Ava Chen",
      "nutritions": {},
      "order": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get fruit by ID action reference](actions/get-fruit-by-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fruityvice/latest/actions/get-fruit-by-id).
