# Loqate: Reverse Geocode International Coordinates

Reverse geocodes international coordinates with Loqate.

```
GET https://connect.mindcloud.co/v1/universal/loqate/latest/actions/reverse-geocode-international-coordinates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loqate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/reverse-geocode-international-coordinates?connectionId=$CONNECTION_ID&latitude=1&longitude=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "1",
  "longitude": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/reverse-geocode-international-coordinates?${params}`, {
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
| `latitude` | number | yes | The latitude for the reverse geocode. |
| `longitude` | number | yes | The longitude for the reverse geocode. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "countryCode": "string",
      "distance": 1,
      "latitude": 1,
      "longitude": 1,
      "postalCode": "string",
      "province": "string",
      "streetName": "Ava Chen",
      "streetNumber": "string"
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
| `distance` | number |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `postalCode` | string |  |
| `province` | string |  |
| `streetName` | string |  |
| `streetNumber` | string |  |

## Native endpoint

Through the native Loqate API, this operation is `GET /Geocoding/International/ReverseGeocode/v2.00/json6.ws` (base URL `https://api.addressy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-geocode-international-coordinates.md) for the provider-specific parameters and requirements.

