# SmugMug Universal API Examples

These examples use the MindCloud API key and SmugMug connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smugMug/latest/actions/get-user?connectionId=$CONNECTION_ID&nickname=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "nickname": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smugMug/latest/actions/get-user?${params}`, {
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
      "Code": 1,
      "Message": "string",
      "Options": {},
      "Response": {}
    }
  ],
  "meta": {}
}
```

See the full [Get User action reference](actions/get-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smugMug/latest/actions/get-user).
