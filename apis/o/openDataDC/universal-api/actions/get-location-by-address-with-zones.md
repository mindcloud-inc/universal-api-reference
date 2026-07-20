# Open Data DC: Get Location By Address With Zones



```
GET https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-location-by-address-with-zones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Data DC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-location-by-address-with-zones?connectionId=$CONNECTION_ID&address=string&zones=string&geo=false" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string",
  "zones": "string",
  "geo": "false"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-location-by-address-with-zones?${params}`, {
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
| `address` | string | yes | Address string value. |
| `zones` | string | yes | Comma-separated zones, for example ward,psa. |
| `geo` | boolean | yes | Whether to include geometry. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Message": "string",
      "Result": {
        "addresses": {
          "0": {
            "address": {
              "properties": {
                "FullAddress": "string",
                "MarId": "string"
              }
            }
          }
        }
      },
      "Success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Message` | string | Provider message. |
| `Result.addresses` | array<object> | Matched address records. |
| `Result.addresses.0.address.properties.FullAddress` | string | Matched full address. |
| `Result.addresses.0.address.properties.MarId` | string | MAR identifier. |
| `Success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native Open Data DC API, this operation is `GET /api/v2.2/locations/:address/:zones/:geo` (base URL `https://datagate.dc.gov/mar/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location-by-address-with-zones.md) for the provider-specific parameters and requirements.

