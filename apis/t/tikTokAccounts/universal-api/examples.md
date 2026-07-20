# TikTok Accounts Universal API Examples

These examples use the MindCloud API key and TikTok Accounts connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Info

Retrieves profile information for the authenticated user in TikTok.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokAccounts/latest/actions/get-user-info?connectionId=$CONNECTION_ID&fields=open_id%2Cavatar_url%2Cdisplay_name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fields": "open_id,avatar_url,display_name"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokAccounts/latest/actions/get-user-info?${params}`, {
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
      "avatar_large_url": "https://example.com",
      "avatar_url": "https://example.com",
      "avatar_url_100": "https://example.com",
      "display_name": "Ava Chen",
      "open_id": "string",
      "union_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User Info action reference](actions/get-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tikTokAccounts/latest/actions/get-user-info).
