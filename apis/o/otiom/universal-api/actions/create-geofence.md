# Otiom: Create Geofence

Creates a new geofence in Otiom.

```
POST https://connect.mindcloud.co/v1/universal/otiom/latest/actions/create-geofence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Otiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/otiom/latest/actions/create-geofence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "points": "12.5683,55.6761,12.5684,55.6761,12.5683,55.6762"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/otiom/latest/actions/create-geofence', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "points": "12.5683,55.6761,12.5684,55.6761,12.5683,55.6762"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Example: `Runtime test geofence`. |
| `points` | object | yes | Polygon coordinates as an array of three to seven [longitude, latitude] pairs. Example: `12.5683,55.6761,12.5684,55.6761,12.5683,55.6762`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `patient` | number | no | Example: `8399`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "administrating": true,
      "id": 1,
      "name": "Ava Chen",
      "patient": 1,
      "patients": [
        1
      ],
      "points": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administrating` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `patient` | number |  |
| `patients` | array<number> |  |
| `points` | array<array> |  |

## Native endpoint

Through the native Otiom API, this operation is `POST /api/geofences/` (base URL `https://api.otiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-geofence.md) for the provider-specific parameters and requirements.

