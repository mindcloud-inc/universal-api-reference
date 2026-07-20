# Lookify Universal API Examples

These examples use the MindCloud API key and Lookify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Lookup Carrier



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lookify/latest/actions/lookup-carrier?connectionId=$CONNECTION_ID&nid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "nid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lookify/latest/actions/lookup-carrier?${params}`, {
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
      "billingPeriod": "string",
      "billingPeriodUsage": 1,
      "carrier": "string",
      "country": "string",
      "nid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Lookup Carrier action reference](actions/lookup-carrier.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lookify/latest/actions/lookup-carrier).
