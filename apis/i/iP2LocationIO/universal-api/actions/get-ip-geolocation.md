# IP2Location IO: Get IP Geolocation



```
GET https://connect.mindcloud.co/v1/universal/iP2LocationIO/latest/actions/get-ip-geolocation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IP2Location IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iP2LocationIO/latest/actions/get-ip-geolocation?connectionId=$CONNECTION_ID&ip=8.8.8.8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "8.8.8.8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iP2LocationIO/latest/actions/get-ip-geolocation?${params}`, {
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
      "city_name": "Ava Chen",
      "country_code": "string",
      "country_name": "Ava Chen",
      "ip": "string",
      "is_proxy": true,
      "latitude": 1,
      "longitude": 1,
      "region_name": "Ava Chen",
      "time_zone": "string",
      "zip_code": "string"
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
| `city_name` | string |  |
| `country_code` | string |  |
| `country_name` | string |  |
| `ip` | string |  |
| `is_proxy` | boolean |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `region_name` | string |  |
| `time_zone` | string |  |
| `zip_code` | string |  |

## Native endpoint

Through the native IP2Location IO API, this operation is `GET /` (base URL `https://api.ip2location.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-geolocation.md) for the provider-specific parameters and requirements.

