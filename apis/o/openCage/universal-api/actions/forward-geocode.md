# OpenCage: Forward Geocode

Finds location details in OpenCage by address or place name.

```
GET https://connect.mindcloud.co/v1/universal/openCage/latest/actions/forward-geocode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenCage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openCage/latest/actions/forward-geocode?connectionId=$CONNECTION_ID&q=Frauenplan%201%2C%2099423%20Weimar%2C%20Germany" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "Frauenplan 1, 99423 Weimar, Germany"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openCage/latest/actions/forward-geocode?${params}`, {
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
| `q` | string | yes | Address, place name, or LOCODE query to geocode. Must be at least two characters. Example: `Frauenplan 1, 99423 Weimar, Germany`. |
| `limit` | number | no | Maximum number of results to return for forward geocoding. Defaults to 10 and can be up to 100. Example: `10`. |
| `countrycode` | string | no | Optional ISO 3166-1 alpha-2 country code, or comma-separated country codes, to restrict forward geocoding results. Example: `de`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bounds` | string | no | Optional bounding box for forward geocoding in min longitude, min latitude, max longitude, max latitude order. Example: `-0.563160,51.280430,0.278970,51.683979`. |
| `language` | string | no | Optional language code to favor in returned results, such as `de`, `pt-BR`, or `native`. Example: `en`. |
| `proximity` | string | no | Optional latitude,longitude hint to bias forward geocoding results toward a location. Example: `52.5432379,13.4142133`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentation": "https://example.com",
      "licenses": [
        {}
      ],
      "rate": {},
      "results": [
        {}
      ],
      "status": {},
      "thanks": "string",
      "timestamp": {},
      "total_results": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentation` | string | OpenCage API documentation URL returned with the response. |
| `licenses` | array<object> | Attribution and license metadata for returned geocoding data. |
| `rate` | object | Rate-limit details returned for accounts with hard limits. |
| `results` | array<object> | Forward geocoding result objects, including formatted address, components, bounds, and geometry. |
| `status` | object | Response status code and message. |
| `thanks` | string | OpenCage thank-you message. |
| `timestamp` | object | Response creation timestamp. |
| `total_results` | number | Total number of forward geocoding results. |

## Native endpoint

Through the native OpenCage API, this operation is `GET /json` (base URL `https://api.opencagedata.com/geocode/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/forward-geocode.md) for the provider-specific parameters and requirements.

