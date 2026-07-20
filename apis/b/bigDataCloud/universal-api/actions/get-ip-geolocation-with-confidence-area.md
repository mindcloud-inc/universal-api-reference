# BigDataCloud: Get IP Geolocation with Confidence Area

Retrieves IP geolocation with confidence area details from BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-ip-geolocation-with-confidence-area
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-ip-geolocation-with-confidence-area?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-ip-geolocation-with-confidence-area?${params}`, {
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
| `ip` | string | no | IPv4 or IPv6 address. If omitted, the caller IP address is assumed. Example: `18.204.48.174`. |
| `localityLanguage` | string | no | Preferred language for locality names in ISO 639-1 format. Default: `en`. Example: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confidence": "string",
      "confidenceArea": [
        {}
      ],
      "country": {},
      "ip": "string",
      "isReachableGlobally": true,
      "lastUpdated": "string",
      "localityLanguageRequested": "string",
      "location": {},
      "network": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confidence` | string | Geolocation confidence level. |
| `confidenceArea` | array<object> | Closed polygon representing the estimated confidence area. |
| `country` | object | Country details for the geolocated IP address. |
| `ip` | string | Requested IP address in string format. |
| `isReachableGlobally` | boolean | Whether the IP address is reachable on the global routing table. |
| `lastUpdated` | string | Time when this IP address geolocation was last assessed. |
| `localityLanguageRequested` | string | Locality language request value used for the response. |
| `location` | object | Estimated geolocation details for the IP address. |
| `network` | object | Network details for the IP address. |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/ip-geolocation-with-confidence` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-geolocation-with-confidence-area.md) for the provider-specific parameters and requirements.

