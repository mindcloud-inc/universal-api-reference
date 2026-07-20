# Cloudmersive: Reverse Geocode Address

Reverse geocodes coordinates into an address in Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/reverse-geocode-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/reverse-geocode-address?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/reverse-geocode-address?${params}`, {
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
| `Latitude` | string | no | Latitude in WGS84 format. |
| `Longitude` | string | no | Longitude in WGS84 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "countryCode": "string",
      "countryFullName": "Ava Chen",
      "postalCode": "string",
      "stateOrProvince": "string",
      "streetAddress": "string",
      "successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `countryCode` | string |  |
| `countryFullName` | string |  |
| `postalCode` | string |  |
| `stateOrProvince` | string |  |
| `streetAddress` | string |  |
| `successful` | boolean |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /validate/address/geocode/reverse` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-geocode-address.md) for the provider-specific parameters and requirements.

