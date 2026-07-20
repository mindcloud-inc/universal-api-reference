# Zubie: Update Place

Updates an existing place in Zubie.

```
PUT https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-place
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-place" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from_time": "string",
  "place_key": "string",
  "to_time": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-place', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from_time": "string",
    "place_key": "string",
    "to_time": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from_time` | string | yes | Start time window in hh:mm format. |
| `place_key` | string | yes | Unique place key. |
| `to_time` | string | yes | End time window in hh:mm format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "category": "string",
      "key": "string",
      "name": "Ava Chen",
      "radius": 1,
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `category` | string |  |
| `key` | string |  |
| `name` | string |  |
| `radius` | number |  |
| `updated` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `POST /place/{place_key}` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-place.md) for the provider-specific parameters and requirements.

