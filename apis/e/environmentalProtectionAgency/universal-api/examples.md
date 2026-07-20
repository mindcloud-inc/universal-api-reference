# Environmental Protection Agency Universal API Examples

These examples use the MindCloud API key and Environmental Protection Agency connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List States

Retrieves states from EPA AQS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/list-states?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/list-states?${params}`, {
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
      "code": "string",
      "value_represented": "string"
    }
  ],
  "meta": {}
}
```

See the full [List States action reference](actions/list-states.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/environmentalProtectionAgency/latest/actions/list-states).
