# Invision Community Universal API Examples

These examples use the MindCloud API key and Invision Community connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Community Info



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-community-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-community-info?${params}`, {
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
      "communityName": "Ava Chen",
      "communityUrl": "https://example.com",
      "ipsApplications": [
        "Ava Chen"
      ],
      "ipsVersion": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Community Info action reference](actions/get-community-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/invisionCommunity/latest/actions/get-community-info).
