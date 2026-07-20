# serviceminder.io Universal API Examples

These examples use the MindCloud API key and serviceminder.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test Echo

Retrieves a test echo response from ServiceMinder.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/test-echo?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/test-echo?${params}`, {
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
      "Message": "string",
      "ResultCode": 1
    }
  ],
  "meta": {}
}
```

See the full [Test Echo action reference](actions/test-echo.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/serviceminderio/latest/actions/test-echo).
