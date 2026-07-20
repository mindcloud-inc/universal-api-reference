# myUplink Universal API Examples

These examples use the MindCloud API key and myUplink connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test Authorized API Availability

Tests authorized API availability in myUplink.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myUplink/latest/actions/test-authorized-api-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myUplink/latest/actions/test-authorized-api-availability?${params}`, {
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

See the full [Test Authorized API Availability action reference](actions/test-authorized-api-availability.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/myUplink/latest/actions/test-authorized-api-availability).
