# ITM Platform Universal API Examples

These examples use the MindCloud API key and ITM Platform connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authentication



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-authentication?${params}`, {
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
      "result": "string",
      "resultStatus": "string",
      "token": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Authentication action reference](actions/get-authentication.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iTMPlatform/latest/actions/get-authentication).
