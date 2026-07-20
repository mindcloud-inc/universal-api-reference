# Greip - Fraud Prevention: Get IP Lookup

Retrieves lookup data for an IP address from Greip.

```
GET https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-ip-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Greip - Fraud Prevention `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-ip-lookup?connectionId=$CONNECTION_ID&ip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-ip-lookup?${params}`, {
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
| `ip` | string | yes | The IPv4 or IPv6 address to inspect. |
| `params` | string | no | Comma-separated response modules to include, such as security, currency, timezone, location, or device. |
| `lang` | string | no | Response language. Greip documents EN, AR, DE, FR, ES, JA, ZH, and RU. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asn": {},
      "bogon": true,
      "cityName": "Ava Chen",
      "continentCode": "string",
      "continentGeoNameID": 1,
      "continentName": "Ava Chen",
      "countryCode": "string",
      "countryGeoNameID": 1,
      "countryName": "Ava Chen",
      "ip": "string",
      "iPNumber": 1,
      "ipType": "string",
      "latitude": "string",
      "longitude": "string",
      "regionName": "Ava Chen",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asn` | object |  |
| `bogon` | boolean |  |
| `cityName` | string |  |
| `continentCode` | string |  |
| `continentGeoNameID` | number |  |
| `continentName` | string |  |
| `countryCode` | string |  |
| `countryGeoNameID` | number |  |
| `countryName` | string |  |
| `ip` | string |  |
| `iPNumber` | number |  |
| `ipType` | string |  |
| `latitude` | string |  |
| `longitude` | string |  |
| `regionName` | string |  |
| `zipCode` | string |  |

## Native endpoint

Through the native Greip - Fraud Prevention API, this operation is `GET /lookup/ip` (base URL `https://greipapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-lookup.md) for the provider-specific parameters and requirements.

