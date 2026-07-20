# Lusha Connect Universal API Examples

These examples use the MindCloud API key and Lusha Connect connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Usage

Retrieves account usage statistics from Lusha Connect.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/get-account-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/get-account-usage?${params}`, {
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
      "usage": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Account Usage action reference](actions/get-account-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lushaConnect/latest/actions/get-account-usage).
