# Qntrl Universal API Examples

These examples use the MindCloud API key and Qntrl connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Organization Details

Retrieves organization details from Qntrl.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/get-organization-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/get-organization-details?${params}`, {
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
      "orgDomain": "string",
      "orgId": "string",
      "orgUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Organization Details action reference](actions/get-organization-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/qntrl/latest/actions/get-organization-details).
