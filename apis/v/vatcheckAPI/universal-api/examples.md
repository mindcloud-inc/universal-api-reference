# VatcheckAPI Universal API Examples

These examples use the MindCloud API key and VatcheckAPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Status

Retrieves the current quota status from VatcheckAPI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vatcheckAPI/latest/actions/check-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vatcheckAPI/latest/actions/check-status?${params}`, {
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
      "account_id": 1,
      "quotas": {
        "grace": {
          "remaining": 1,
          "total": 1,
          "used": 1
        },
        "month": {
          "remaining": 1,
          "total": 1,
          "used": 1
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Check Status action reference](actions/check-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vatcheckAPI/latest/actions/check-status).
