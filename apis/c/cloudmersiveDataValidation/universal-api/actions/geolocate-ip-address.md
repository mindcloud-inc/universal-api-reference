# Cloudmersive Data Validation: Geolocate IP Address

Geolocates an IP address with Cloudmersive Data Validation.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/geolocate-ip-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Data Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/geolocate-ip-address?connectionId=$CONNECTION_ID&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/geolocate-ip-address?${params}`, {
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
| `value` | string | yes | IP address to geolocate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "City": "string",
      "CountryCode": "string",
      "CountryName": "Ava Chen",
      "Latitude": 1,
      "Longitude": 1,
      "RegionCode": "string",
      "RegionName": "Ava Chen",
      "TimezoneStandardName": "Ava Chen",
      "ZipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `City` | string |  |
| `CountryCode` | string |  |
| `CountryName` | string |  |
| `Latitude` | number |  |
| `Longitude` | number |  |
| `RegionCode` | string |  |
| `RegionName` | string |  |
| `TimezoneStandardName` | string |  |
| `ZipCode` | string |  |

## Native endpoint

Through the native Cloudmersive Data Validation API, this operation is `POST /validate/ip/geolocate` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/geolocate-ip-address.md) for the provider-specific parameters and requirements.

