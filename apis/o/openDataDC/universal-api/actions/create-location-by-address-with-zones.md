# Open Data DC: Create Location By Address With Zones



```
POST https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-location-by-address-with-zones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Data DC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-location-by-address-with-zones" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": "string",
  "zones": "string",
  "geo": "false"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-location-by-address-with-zones', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": "string",
    "zones": "string",
    "geo": "false"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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
      "0": {
        "addresses": [
          {}
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `0` | object | Location result item. |
| `0.addresses` | array<object> | Matched address records. |

## Native endpoint

Through the native Open Data DC API, this operation is `POST /api/v2.2/locations/:address/:zones/:geo` (base URL `https://datagate.dc.gov/mar/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-location-by-address-with-zones.md) for the provider-specific parameters and requirements.

