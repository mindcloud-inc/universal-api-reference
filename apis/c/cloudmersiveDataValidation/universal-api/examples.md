# Cloudmersive Data Validation Universal API Examples

These examples use the MindCloud API key and Cloudmersive Data Validation connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get IP Intelligence

Retrieves IP intelligence from Cloudmersive Data Validation.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/get-ip-intelligence?connectionId=$CONNECTION_ID&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/get-ip-intelligence?${params}`, {
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
      "CurrencyCode": "string",
      "CurrencyName": "Ava Chen",
      "IsBot": true,
      "IsEU": true,
      "IsThreat": true,
      "IsTorNode": true,
      "Location": {
        "City": "string",
        "CountryCode": "string",
        "CountryName": "Ava Chen",
        "Latitude": 1,
        "Longitude": 1,
        "RegionCode": "string",
        "RegionName": "Ava Chen",
        "TimezoneStandardName": "Ava Chen",
        "ZipCode": "string"
      },
      "RegionArea": "string",
      "SubregionArea": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get IP Intelligence action reference](actions/get-ip-intelligence.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudmersiveDataValidation/latest/actions/get-ip-intelligence).
