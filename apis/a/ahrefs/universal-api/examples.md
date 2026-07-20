# Ahrefs Universal API Examples

These examples use the MindCloud API key and Ahrefs connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Limits And Usage



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-limits-and-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-limits-and-usage?${params}`, {
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
      "limits_and_usage": {
        "api_key_expiration_date": "2026-05-07T12:00:00.000Z",
        "subscription": "string",
        "units_limit_api_key": 1,
        "units_limit_workspace": 1,
        "units_usage_api_key": 1,
        "units_usage_workspace": 1,
        "usage_reset_date": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Limits And Usage action reference](actions/get-limits-and-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ahrefs/latest/actions/get-limits-and-usage).
