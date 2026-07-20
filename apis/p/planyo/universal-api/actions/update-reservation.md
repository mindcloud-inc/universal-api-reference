# Planyo: Update Reservation

Updates an existing reservation in Planyo.

```
PUT https://connect.mindcloud.co/v1/universal/planyo/latest/actions/update-reservation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planyo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/update-reservation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reservationId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planyo/latest/actions/update-reservation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reservationId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reservationId` | number | yes |  |
| `startTime` | string | no |  |
| `endTime` | string | no |  |
| `resourceId` | number | no |  |
| `quantity` | number | no |  |
| `adminMode` | boolean | no |  |
| `sendNotifications` | boolean | no |  |
| `recalculatePrice` | boolean | no |  |
| `comments` | string | no |  |
| `userId` | number | no |  |
| `assignment1` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1,
      "warningText": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number |  |
| `warningText` | string |  |

## Native endpoint

Through the native Planyo API, this operation is `GET /` (base URL `https://www.planyo.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-reservation.md) for the provider-specific parameters and requirements.

