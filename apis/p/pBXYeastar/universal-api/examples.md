# PBX Yeastar Universal API Examples

These examples use the MindCloud API key and PBX Yeastar connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Query PBX Information

Retrieves PBX information from PBX Yeastar.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pBXYeastar/latest/actions/query-pbx-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pBXYeastar/latest/actions/query-pbx-information?${params}`, {
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
      "data": {},
      "errcode": 1,
      "errmsg": "string"
    }
  ],
  "meta": {}
}
```

See the full [Query PBX Information action reference](actions/query-pbx-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pBXYeastar/latest/actions/query-pbx-information).
