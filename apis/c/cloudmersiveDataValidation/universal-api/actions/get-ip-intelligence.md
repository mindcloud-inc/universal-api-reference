# Cloudmersive Data Validation: Get IP Intelligence

Retrieves IP intelligence from Cloudmersive Data Validation.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/get-ip-intelligence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Data Validation `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `value` | string | yes | IP address to inspect. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CurrencyCode` | string |  |
| `CurrencyName` | string |  |
| `IsBot` | boolean |  |
| `IsEU` | boolean |  |
| `IsThreat` | boolean |  |
| `IsTorNode` | boolean |  |
| `Location.City` | string |  |
| `Location.CountryCode` | string |  |
| `Location.CountryName` | string |  |
| `Location.Latitude` | number |  |
| `Location.Longitude` | number |  |
| `Location.RegionCode` | string |  |
| `Location.RegionName` | string |  |
| `Location.TimezoneStandardName` | string |  |
| `Location.ZipCode` | string |  |
| `RegionArea` | string |  |
| `SubregionArea` | string |  |

## Native endpoint

Through the native Cloudmersive Data Validation API, this operation is `POST /validate/ip/intelligence` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-intelligence.md) for the provider-specific parameters and requirements.

