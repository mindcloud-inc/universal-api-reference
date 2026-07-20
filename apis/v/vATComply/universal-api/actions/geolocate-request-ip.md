# VAT Comply: Geolocate Request IP

Retrieves request IP geolocation from VAT Comply.

```
GET https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/geolocate-request-ip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VAT Comply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/geolocate-request-ip?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/geolocate-request-ip?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "capital": "string",
      "country_code": "string",
      "currency": "string",
      "emoji": "string",
      "ip": "string",
      "iso2": "string",
      "iso3": "string",
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "numeric_code": 1,
      "phone_code": "string",
      "region": "string",
      "subregion": "string",
      "tld": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capital` | string |  |
| `country_code` | string |  |
| `currency` | string |  |
| `emoji` | string |  |
| `ip` | string |  |
| `iso2` | string |  |
| `iso3` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `name` | string |  |
| `numeric_code` | number |  |
| `phone_code` | string |  |
| `region` | string |  |
| `subregion` | string |  |
| `tld` | string |  |

## Native endpoint

Through the native VAT Comply API, this operation is `GET /geolocate` (base URL `https://api.vatcomply.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/geolocate-request-ip.md) for the provider-specific parameters and requirements.

