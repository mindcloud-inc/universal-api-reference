# Numverify Universal API Examples

These examples use the MindCloud API key and Numverify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Supported Countries

Retrieves supported countries and dialing codes from Numverify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/numverify/latest/actions/list-supported-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/numverify/latest/actions/list-supported-countries?${params}`, {
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
      "countryCode": "string",
      "countryName": "Ava Chen",
      "diallingCode": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Supported Countries action reference](actions/list-supported-countries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/numverify/latest/actions/list-supported-countries).
