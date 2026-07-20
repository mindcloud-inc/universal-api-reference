# Zubie: Create Place

Creates a place in Zubie.

```
POST https://connect.mindcloud.co/v1/universal/zubie/latest/actions/create-place
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/create-place" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "active_weekdays[]": [
    1
  ],
  "from_time": "string",
  "to_time": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zubie/latest/actions/create-place', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "active_weekdays[]": [1],
    "from_time": "string",
    "to_time": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `active_weekdays[]` | array<number> | yes | Days of week to detect geofence events. |
| `from_time` | string | yes | Start time window in hh:mm format. |
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

Through the native Zubie API, this operation is `POST /places` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-place.md) for the provider-specific parameters and requirements.

