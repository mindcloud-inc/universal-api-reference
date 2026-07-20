# IFTTT Universal API Examples

These examples use the MindCloud API key and IFTTT connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Service and User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iFTTT/latest/actions/get-current-service-and-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iFTTT/latest/actions/get-current-service-and-user?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Current Service and User action reference](actions/get-current-service-and-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iFTTT/latest/actions/get-current-service-and-user).
