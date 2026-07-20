# Addressfinder Universal API Examples

These examples use the MindCloud API key and Addressfinder connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List AU Address Suggestions

Finds Australian address suggestions in Addressfinder by partial query.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/list-au-address-suggestions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/list-au-address-suggestions?${params}`, {
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

See the full [List AU Address Suggestions action reference](actions/list-au-address-suggestions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/addressfinder/latest/actions/list-au-address-suggestions).
