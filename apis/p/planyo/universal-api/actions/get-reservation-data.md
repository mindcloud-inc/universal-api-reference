# Planyo: Get Reservation Data

Retrieves reservation data from Planyo.

```
GET https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-reservation-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planyo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-reservation-data?connectionId=$CONNECTION_ID&reservationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reservationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-reservation-data?${params}`, {
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
| `reservationId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "adminNotes": "string",
      "amountPaid": 1,
      "cartId": 1,
      "city": "string",
      "country": "string",
      "creationTime": "string",
      "creationWebsite": "string",
      "currency": "string",
      "customColor": "string",
      "customProducts": [
        {}
      ],
      "discount": 1,
      "email": "ava@example.com",
      "endTime": "string",
      "firstName": "Ava",
      "lastName": "Chen",
      "logEvents": [
        {}
      ],
      "mobileNumber": "string",
      "name": "Ava Chen",
      "nightReservation": "string",
      "notificationsSent": [
        {}
      ],
      "originalPrice": 1,
      "phoneNumber": "string",
      "pppRs": "string",
      "properties": {},
      "quantity": 1,
      "regularProducts": [
        {}
      ],
      "resourceId": 1,
      "siteId": 1,
      "startTime": "string",
      "state": "string",
      "status": 1,
      "totalPrice": 1,
      "unitAssignment": "string",
      "userId": 1,
      "userNotes": "string",
      "userText": "string",
      "wantsShare": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `adminNotes` | string |  |
| `amountPaid` | number |  |
| `cartId` | number |  |
| `city` | string |  |
| `country` | string |  |
| `creationTime` | string |  |
| `creationWebsite` | string |  |
| `currency` | string |  |
| `customColor` | string |  |
| `customProducts` | array<object> |  |
| `discount` | number |  |
| `email` | string |  |
| `endTime` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `logEvents` | array<object> |  |
| `mobileNumber` | string |  |
| `name` | string |  |
| `nightReservation` | string |  |
| `notificationsSent` | array<object> |  |
| `originalPrice` | number |  |
| `phoneNumber` | string |  |
| `pppRs` | string |  |
| `properties` | object |  |
| `quantity` | number |  |
| `regularProducts` | array<object> |  |
| `resourceId` | number |  |
| `siteId` | number |  |
| `startTime` | string |  |
| `state` | string |  |
| `status` | number |  |
| `totalPrice` | number |  |
| `unitAssignment` | string |  |
| `userId` | number |  |
| `userNotes` | string |  |
| `userText` | string |  |
| `wantsShare` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native Planyo API, this operation is `GET /` (base URL `https://www.planyo.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reservation-data.md) for the provider-specific parameters and requirements.

