# VAT Comply Universal API Examples

These examples use the MindCloud API key and VAT Comply connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check API Health

Retrieves API health status from VAT Comply.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/check-api-health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/check-api-health?${params}`, {
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check API Health action reference](actions/check-api-health.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vATComply/latest/actions/check-api-health).
