# Cloudmersive Currency Universal API Examples

These examples use the MindCloud API key and Cloudmersive Currency connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Available Currencies

Retrieves available currencies from Cloudmersive Currency.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveCurrency/latest/actions/list-available-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveCurrency/latest/actions/list-available-currencies?${params}`, {
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
      "Currencies": [
        {
          "CountryISOTwoLetterCode": "string",
          "CountryName": "Ava Chen",
          "CountryThreeLetterCode": "string",
          "CurrencyEnglishName": "Ava Chen",
          "CurrencySymbol": "string",
          "IsEuropeanUnionMember": true,
          "ISOCurrencyCode": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Available Currencies action reference](actions/list-available-currencies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudmersiveCurrency/latest/actions/list-available-currencies).
