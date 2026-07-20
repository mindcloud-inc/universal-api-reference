# Rosette Text Analytics Universal API Examples

These examples use the MindCloud API key and Rosette Text Analytics connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check API Status



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/check-api-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/check-api-status?${params}`, {
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
      "message": "string",
      "time": 1
    }
  ],
  "meta": {}
}
```

See the full [Check API Status action reference](actions/check-api-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rosetteTextAnalytics/latest/actions/check-api-status).
