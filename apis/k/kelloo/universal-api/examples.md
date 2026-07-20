# Kelloo Universal API Examples

These examples use the MindCloud API key and Kelloo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Application Configuration

Retrieves application configuration details from Kelloo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kelloo/latest/actions/get-application-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kelloo/latest/actions/get-application-configuration?${params}`, {
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

See the full [Get Application Configuration action reference](actions/get-application-configuration.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kelloo/latest/actions/get-application-configuration).
