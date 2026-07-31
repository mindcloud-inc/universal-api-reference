# DiceBear Universal API Examples

These examples use the MindCloud API key and DiceBear connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Avatar Metadata



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diceBear/latest/actions/get-avatar-metadata?connectionId=$CONNECTION_ID&styleName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "styleName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diceBear/latest/actions/get-avatar-metadata?${params}`, {
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
      "options": {},
      "svg": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Avatar Metadata action reference](actions/get-avatar-metadata.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/diceBear/latest/actions/get-avatar-metadata).
