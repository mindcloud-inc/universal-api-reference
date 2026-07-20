# Open Data DC: Get Nearest Locations By Coordinates



```
GET https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-nearest-locations-by-coordinates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Data DC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-nearest-locations-by-coordinates?connectionId=$CONNECTION_ID&latlong=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latlong": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-nearest-locations-by-coordinates?${params}`, {
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
| `latlong` | string | yes | Latitude and longitude, for example 38.888,-77.00. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Message": "string",
      "Result": {
        "0": {
          "address": {
            "properties": {
              "FullAddress": "string"
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
| `Result` | array<object> | Nearest address results. |
| `Result.0.address.properties.FullAddress` | string | Matched full address. |
| `Success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native Open Data DC API, this operation is `GET /api/v2.2/locations/:latlong` (base URL `https://datagate.dc.gov/mar/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-nearest-locations-by-coordinates.md) for the provider-specific parameters and requirements.

