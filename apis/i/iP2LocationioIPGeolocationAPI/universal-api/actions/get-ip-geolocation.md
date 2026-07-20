# IP2Location.io IP Geolocation: Get IP Geolocation

Retrieves IP geolocation details from IP2Location.io.

```
GET https://connect.mindcloud.co/v1/universal/iP2LocationioIPGeolocationAPI/latest/actions/get-ip-geolocation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IP2Location.io IP Geolocation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iP2LocationioIPGeolocationAPI/latest/actions/get-ip-geolocation?connectionId=$CONNECTION_ID&ip=8.8.8.8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "8.8.8.8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iP2LocationioIPGeolocationAPI/latest/actions/get-ip-geolocation?${params}`, {
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
| `ip` | string | yes | IPv4 or IPv6 address to look up. Example: `8.8.8.8`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lang` | string | no | ISO 639-1 language code for translated continent, country, region, and city names. Available on Plus and Security plans only. Example: `fr`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "as": "string",
      "asn": "string",
      "cityName": "Ava Chen",
      "countryCode": "string",
      "countryName": "Ava Chen",
      "ip": "string",
      "isProxy": true,
      "latitude": 1,
      "longitude": 1,
      "regionName": "Ava Chen",
      "timeZone": "string",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `as` | string |  |
| `asn` | string |  |
| `cityName` | string |  |
| `countryCode` | string |  |
| `countryName` | string |  |
| `ip` | string |  |
| `isProxy` | boolean |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `regionName` | string |  |
| `timeZone` | string |  |
| `zipCode` | string |  |

## Native endpoint

Through the native IP2Location.io IP Geolocation API, this operation is `GET /` (base URL `https://api.ip2location.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-geolocation.md) for the provider-specific parameters and requirements.

