# Open Data DC: Create Nearest Locations From Body



```
POST https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-nearest-locations-from-body
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Data DC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-nearest-locations-from-body" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "latlong": "string",
  "count": 1,
  "geo": "false"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-nearest-locations-from-body', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "latlong": "string",
    "count": 1,
    "geo": "false"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `latlong` | string | yes | Latitude/longitude string value in the request JSON object. Provider runtime expects the singular key `latlong`. |
| `count` | number | yes | Nearest location number. |
| `geo` | boolean | yes | Whether to include geometry. Default: `false`. |

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

Through the native Open Data DC API, this operation is `POST /api/v2.2/locations/:count/:geo` (base URL `https://datagate.dc.gov/mar/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-nearest-locations-from-body.md) for the provider-specific parameters and requirements.

