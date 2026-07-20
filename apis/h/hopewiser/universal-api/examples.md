# Hopewiser Universal API Examples

These examples use the MindCloud API key and Hopewiser connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Master Address Files



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hopewiser/latest/actions/list-master-address-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hopewiser/latest/actions/list-master-address-files?${params}`, {
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Master Address Files action reference](actions/list-master-address-files.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hopewiser/latest/actions/list-master-address-files).
