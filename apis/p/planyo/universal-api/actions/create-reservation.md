# Planyo: Create Reservation

Creates a new reservation in Planyo.

```
POST https://connect.mindcloud.co/v1/universal/planyo/latest/actions/create-reservation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planyo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/create-reservation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": 1,
  "startTime": "string",
  "endTime": "string",
  "quantity": 1,
  "email": "ava@example.com",
  "firstName": "Ava"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planyo/latest/actions/create-reservation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": 1,
    "startTime": "string",
    "endTime": "string",
    "quantity": 1,
    "email": "ava@example.com",
    "firstName": "Ava"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceId` | number | yes |  |
| `startTime` | string | yes |  |
| `endTime` | string | yes |  |
| `quantity` | number | yes |  |
| `email` | string | yes |  |
| `firstName` | string | yes |  |
| `lastName` | string | no |  |
| `adminMode` | boolean | no |  |
| `sendNotifications` | boolean | no |  |
| `forceStatus` | number | no |  |
| `wantsShare` | string | no |  |
| `userId` | number | no |  |
| `userNotes` | string | no |  |
| `adminNotes` | string | no |  |
| `assignment1` | string | no |  |
| `addToWaitlist` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "discount": 1,
      "originalPrice": 1,
      "properties": {},
      "reservationId": 1,
      "resourceId": 1,
      "status": 1,
      "totalPrice": 1,
      "userText": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `discount` | number |  |
| `originalPrice` | number |  |
| `properties` | object |  |
| `reservationId` | number |  |
| `resourceId` | number |  |
| `status` | number |  |
| `totalPrice` | number |  |
| `userText` | string |  |

## Native endpoint

Through the native Planyo API, this operation is `GET /` (base URL `https://www.planyo.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reservation.md) for the provider-specific parameters and requirements.

