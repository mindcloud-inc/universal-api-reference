# Open Notify Universal API Examples

These examples use the MindCloud API key and Open Notify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current ISS Position



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openNotify/latest/actions/get-current-iss-position?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openNotify/latest/actions/get-current-iss-position?${params}`, {
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
      "iss_position": {},
      "message": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Current ISS Position action reference](actions/get-current-iss-position.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openNotify/latest/actions/get-current-iss-position).
