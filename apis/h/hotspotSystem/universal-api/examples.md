# HotspotSystem Universal API Examples

These examples use the MindCloud API key and HotspotSystem connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Credentials

Verifies HotspotSystem credentials and retrieves owner details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hotspotSystem/latest/actions/verify-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hotspotSystem/latest/actions/verify-credentials?${params}`, {
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
      "operator": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [Verify Credentials action reference](actions/verify-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hotspotSystem/latest/actions/verify-credentials).
