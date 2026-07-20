# Loqate: Get Country From Coordinates

Retrieves a country from coordinates with Loqate.

```
GET https://connect.mindcloud.co/v1/universal/loqate/latest/actions/get-country-from-coordinates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loqate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/get-country-from-coordinates?connectionId=$CONNECTION_ID&latitude=1&longitude=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "1",
  "longitude": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/get-country-from-coordinates?${params}`, {
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
| `latitude` | number | yes | The latitude to search against. |
| `longitude` | number | yes | The longitude to search against. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countryIso2": "string",
      "countryIso3": "string",
      "countryIsoNumber": 1,
      "countryName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryIso2` | string |  |
| `countryIso3` | string |  |
| `countryIsoNumber` | number |  |
| `countryName` | string |  |

## Native endpoint

Through the native Loqate API, this operation is `GET /Geocoding/International/PositionToCountry/v1.00/json6.ws` (base URL `https://api.addressy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-country-from-coordinates.md) for the provider-specific parameters and requirements.

