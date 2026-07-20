# Planyo: Can Make Reservation

Checks whether a reservation can be made in Planyo.

```
GET https://connect.mindcloud.co/v1/universal/planyo/latest/actions/can-make-reservation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planyo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/can-make-reservation?connectionId=$CONNECTION_ID&resourceId=1&startTime=string&endTime=string&quantity=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "1",
  "startTime": "string",
  "endTime": "string",
  "quantity": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planyo/latest/actions/can-make-reservation?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceId` | number | yes |  |
| `startTime` | string | yes |  |
| `endTime` | string | yes |  |
| `quantity` | number | yes |  |
| `assignment1` | string | no |  |
| `adminMode` | boolean | no |  |
| `wantsShare` | string | no |  |
| `userId` | number | no |  |
| `userEmail` | string | no |  |
| `excludedReservationId` | number | no |  |
| `returnAvailability` | boolean | no |  |
| `returnPrice` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isReservationPossible": true,
      "isResourceAvailable": true,
      "price": "string",
      "problemTime": "string",
      "reason": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isReservationPossible` | boolean |  |
| `isResourceAvailable` | boolean |  |
| `price` | string |  |
| `problemTime` | string |  |
| `reason` | string |  |

## Native endpoint

Through the native Planyo API, this operation is `GET /` (base URL `https://www.planyo.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/can-make-reservation.md) for the provider-specific parameters and requirements.

