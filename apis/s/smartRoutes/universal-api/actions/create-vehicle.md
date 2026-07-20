# SmartRoutes: Create Vehicle



```
POST https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/create-vehicle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartRoutes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/create-vehicle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "availability": "0",
  "startLocation": "0",
  "endLocation": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/create-vehicle', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "availability": "0",
    "startLocation": "0",
    "endLocation": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Name of the vehicle. |
| `availability` | string | yes | Availability status of the vehicle. One of: `0`, `1`, `2`. |
| `startLocation` | string | yes | Location type where the vehicle starts. One of: `0`, `1`, `2`. |
| `endLocation` | string | yes | Location type where the vehicle ends. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "availability": "string",
      "break": true,
      "capacities": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "endLocation": "string",
      "id": 1,
      "name": "Ava Chen",
      "shift": [
        {}
      ],
      "skills": [
        "string"
      ],
      "startLocation": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the vehicle is active. |
| `availability` | string | Vehicle availability mode. |
| `break` | boolean | Whether the vehicle currently has a break configured. |
| `capacities` | array<object> | Vehicle capacities. |
| `created` | date | Vehicle creation timestamp. |
| `endLocation` | string | Vehicle end location type. |
| `id` | number | SmartRoutes vehicle identifier. |
| `name` | string | Vehicle name. |
| `shift` | array<object> | Vehicle shift settings. |
| `skills` | array<string> | Vehicle skills. |
| `startLocation` | string | Vehicle start location type. |
| `updated` | date | Vehicle updated timestamp. |

## Native endpoint

Through the native SmartRoutes API, this operation is `POST /vehicles` (base URL `https://api.smartroutes.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vehicle.md) for the provider-specific parameters and requirements.

