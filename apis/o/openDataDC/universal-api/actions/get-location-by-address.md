# Open Data DC: Get Location By Address



```
GET https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-location-by-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Data DC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-location-by-address?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-location-by-address?${params}`, {
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
                "Latitude": 1,
                "Longitude": 1,
                "MarId": "string",
                "Ward": "string"
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
| `Message` | string | Provider message when present. |
| `Result.addresses` | array<object> | Matched address records with geometry and zones. |
| `Result.addresses.0.address.properties.FullAddress` | string | Matched full address. |
| `Result.addresses.0.address.properties.Latitude` | number | Latitude. |
| `Result.addresses.0.address.properties.Longitude` | number | Longitude. |
| `Result.addresses.0.address.properties.MarId` | string | Master Address Repository identifier. |
| `Result.addresses.0.address.properties.Ward` | string | Ward value when included. |
| `Success` | boolean | Whether the MAR lookup succeeded. |

## Native endpoint

Through the native Open Data DC API, this operation is `GET /api/v2.2/locations/:address` (base URL `https://datagate.dc.gov/mar/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location-by-address.md) for the provider-specific parameters and requirements.

