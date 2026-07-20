# The Org Universal API Examples

These examples use the MindCloud API key and The Org connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Usage

Retrieves current API usage from The Org.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/get-current-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/get-current-usage?${params}`, {
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
      "data": {
        "additionalCredits": 1,
        "creditOverages": 1,
        "planCredits": 1,
        "planInterval": "string",
        "planResetDate": "string",
        "unlimited": true
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Current Usage action reference](actions/get-current-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/theOrg/latest/actions/get-current-usage).
