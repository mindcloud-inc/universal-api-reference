# Precisely: Location By IP Address

Retrieves location coordinates from Precisely by IP address.

```
GET https://connect.mindcloud.co/v1/universal/precisely/latest/actions/location-by-ip-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Precisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/precisely/latest/actions/location-by-ip-address?connectionId=$CONNECTION_ID&ipAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ipAddress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/precisely/latest/actions/location-by-ip-address?${params}`, {
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
| `ipAddress` | string | yes | Public IPv4 or IPv6 address to geolocate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accuracy": {
        "unit": "string",
        "value": "string"
      },
      "geometry": {
        "coordinates": [
          1
        ],
        "type": "string"
      },
      "ipInfo": {
        "ipAddress": "string",
        "network": {
          "connectionType": "string",
          "ipRouteType": "string",
          "organization": "string"
        },
        "place": {
          "city": {
            "value": "string"
          },
          "continent": "string",
          "country": {
            "code": "string",
            "value": "string"
          },
          "postCode": "string",
          "state": {
            "value": "string"
          }
        },
        "proxy": {
          "anonymizerStatus": "string",
          "level": "string",
          "type": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accuracy.unit` | string | Unit used for the reported geolocation accuracy. |
| `accuracy.value` | string | Reported accuracy value. |
| `geometry.coordinates` | array<number> | Longitude and latitude coordinates. |
| `geometry.type` | string | GeoJSON geometry type. |
| `ipInfo.ipAddress` | string | Queried IP address. |
| `ipInfo.network.connectionType` | string | Detected connection type. |
| `ipInfo.network.ipRouteType` | string | Detected IP routing classification. |
| `ipInfo.network.organization` | string | Network organization. |
| `ipInfo.place.city.value` | string | Detected city. |
| `ipInfo.place.continent` | string | Detected continent. |
| `ipInfo.place.country.code` | string | Detected country code. |
| `ipInfo.place.country.value` | string | Detected country name. |
| `ipInfo.place.postCode` | string | Detected postal code. |
| `ipInfo.place.state.value` | string | Detected state or province. |
| `ipInfo.proxy.anonymizerStatus` | string | Proxy anonymizer status. |
| `ipInfo.proxy.level` | string | Proxy anonymity level. |
| `ipInfo.proxy.type` | string | Detected proxy type. |

## Native endpoint

Through the native Precisely API, this operation is `GET /geolocation/v1/location/byipaddress` (base URL `https://api.precisely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/location-by-ip-address.md) for the provider-specific parameters and requirements.

