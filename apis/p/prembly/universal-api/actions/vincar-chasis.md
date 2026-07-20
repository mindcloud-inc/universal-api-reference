# Prembly: VIN/CAR CHASIS

Creates a VIN or chassis verification in Prembly.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/vincar-chasis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/vincar-chasis" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/vincar-chasis', {
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
      "country_name": "Ava Chen",
      "format_name": "Ava Chen",
      "is_valid": true,
      "lookup_data": {
        "address": "string",
        "name": "Ava Chen"
      },
      "tin_compact": "string",
      "tin_standard": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country_name` | string |  |
| `format_name` | string |  |
| `is_valid` | boolean |  |
| `lookup_data.address` | string |  |
| `lookup_data.name` | string |  |
| `tin_compact` | string |  |
| `tin_standard` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /verification/vehicle/vin` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/vincar-chasis.md) for the provider-specific parameters and requirements.

