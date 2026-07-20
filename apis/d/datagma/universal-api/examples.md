# Datagma Universal API Examples

These examples use the MindCloud API key and Datagma connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credit

Retrieves account credit details from Datagma.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datagma/latest/actions/get-credit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datagma/latest/actions/get-credit?${params}`, {
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
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Credit action reference](actions/get-credit.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/datagma/latest/actions/get-credit).
