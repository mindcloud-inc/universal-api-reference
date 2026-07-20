# Address Auto-Complete by Fetchify Universal API Examples

These examples use the MindCloud API key and Address Auto-Complete by Fetchify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Supported Countries

Retrieves supported address countries from Fetchify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addressAutoCompleteByFetchify/latest/actions/list-supported-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addressAutoCompleteByFetchify/latest/actions/list-supported-countries?${params}`, {
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
      "countries": [
        {
          "code": "string",
          "countryName": "Ava Chen",
          "intlLongName": "Ava Chen",
          "iso31661Alpha2": "string",
          "iso31661Alpha3": "string",
          "iso31661Numeric3": 1,
          "officialName": "Ava Chen",
          "shortCode": "string"
        }
      ],
      "ipLocation": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Supported Countries action reference](actions/list-supported-countries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/addressAutoCompleteByFetchify/latest/actions/list-supported-countries).
