# Dolibarr Universal API Examples

These examples use the MindCloud API key and Dolibarr connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Status

Retrieves status information for the Dolibarr instance.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-status?${params}`, {
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
      "success": {
        "access_locked": "string",
        "code": 1,
        "dolibarr_version": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Status action reference](actions/get-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dolibarr/latest/actions/get-status).
