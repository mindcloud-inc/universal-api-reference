# Zeo Route Planner: Create Stops

Creates stops in Zeo Route Planner.

```
POST https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/create-stops
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeo Route Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/create-stops" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stops[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/create-stops', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stops[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stops[]` | array<object> | yes | Stops to create as an array of stop objects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | HTTP-style success code returned by Zeo after adding stops. |
| `message` | string | Human-readable Zeo confirmation message for the stop create request. |
| `status` | boolean | Whether Zeo accepted the stop payload. |

## Native endpoint

Through the native Zeo Route Planner API, this operation is `POST /api/v5/route_stop` (base URL `https://zeorouteplanner.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-stops.md) for the provider-specific parameters and requirements.

