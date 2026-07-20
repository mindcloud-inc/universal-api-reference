# Infoplus: Create Location Footprint

Creates a new location footprint in Infoplus.

```
POST https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/create-location-footprint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infoplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/create-location-footprint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/create-location-footprint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "depth": 1,
      "height": 1,
      "id": 1,
      "name": "Ava Chen",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `depth` | number |  |
| `height` | number |  |
| `id` | number |  |
| `name` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Infoplus API, this operation is `POST /locationFootprint` (base URL `https://luxomo.infopluswms.com/infoplus-wms/api/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-location-footprint.md) for the provider-specific parameters and requirements.

