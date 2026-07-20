# EODHD Universal API Examples

These examples use the MindCloud API key and EODHD connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Supported Exchanges

Retrieves supported exchanges from EODHD API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-supported-exchanges?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-supported-exchanges?${params}`, {
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
      "Code": "string",
      "Country": "string",
      "CountryISO2": "string",
      "CountryISO3": "string",
      "Currency": "string",
      "Name": "Ava Chen",
      "OperatingMIC": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Supported Exchanges action reference](actions/list-supported-exchanges.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eODHDAPI/latest/actions/list-supported-exchanges).
