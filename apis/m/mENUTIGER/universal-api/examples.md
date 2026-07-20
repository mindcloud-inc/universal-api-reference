# MENU TIGER Universal API Examples

These examples use the MindCloud API key and MENU TIGER connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Integration Status



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mENUTIGER/latest/actions/get-integration-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mENUTIGER/latest/actions/get-integration-status?${params}`, {
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
      "data": {
        "name": "Ava Chen",
        "restaurantUrl": "https://example.com"
      },
      "msg": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Get Integration Status action reference](actions/get-integration-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mENUTIGER/latest/actions/get-integration-status).
