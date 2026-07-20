# Envoy for Visitors: Create Work Schedule

Creates a new work schedule in Envoy for Visitors.

```
POST https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/create-work-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoy for Visitors `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/create-work-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/create-work-schedule', {
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
      "arrivedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "departedAt": "2026-05-07T12:00:00.000Z",
      "expectedArrivalAt": "2026-05-07T12:00:00.000Z",
      "expectedDepartureAt": "2026-05-07T12:00:00.000Z",
      "flowId": "string",
      "id": "string",
      "locationId": "string",
      "registrationURL": "https://example.com",
      "reservations": {},
      "scheduledFor": {},
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `arrivedAt` | date |  |
| `createdAt` | date |  |
| `departedAt` | date |  |
| `expectedArrivalAt` | date |  |
| `expectedDepartureAt` | date |  |
| `flowId` | string |  |
| `id` | string |  |
| `locationId` | string |  |
| `registrationURL` | string |  |
| `reservations` | object |  |
| `scheduledFor` | object |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Envoy for Visitors API, this operation is `POST /work-schedules` (base URL `https://api.envoy.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-work-schedule.md) for the provider-specific parameters and requirements.

