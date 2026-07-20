# Starfish: Create Reservation

Creates a new reservation in Starfish.

```
POST https://connect.mindcloud.co/v1/universal/starfish/latest/actions/create-reservation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starfish `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/create-reservation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accommodationId": 1,
  "arrival": "string",
  "departure": "string",
  "persons": 1,
  "lastName": "Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starfish/latest/actions/create-reservation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accommodationId": 1,
    "arrival": "string",
    "departure": "string",
    "persons": 1,
    "lastName": "Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accommodationId` | number | yes | Accommodation ID. |
| `arrival` | string | yes | Reservation arrival date. |
| `departure` | string | yes | Reservation departure date. |
| `persons` | number | yes | Number of persons. |
| `lastName` | string | yes | Main traveler last name. |
| `email` | string | yes | Main traveler email. |
| `placeId` | number | no | Place ID. |
| `mainTraveler` | string | no | Stringified JSON for the main traveler. |
| `force` | string | no | Force reservation creation. |
| `forcedRows` | string | no | Stringified JSON array of forced reservation rows. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accommodation": {},
      "accommodationId": 1,
      "adminId": 1,
      "arrival": "2026-05-07T12:00:00.000Z",
      "booker": {},
      "categoryId": 1,
      "chainId": 1,
      "channel": {},
      "channelId": 1,
      "contact": {},
      "contactId": 1,
      "coTravelers": {},
      "createDate": "2026-05-07T12:00:00.000Z",
      "departure": "2026-05-07T12:00:00.000Z",
      "draftId": "string",
      "groupId": 1,
      "id": 1,
      "invoices": [
        {}
      ],
      "lastModified": "2026-05-07T12:00:00.000Z",
      "mainTraveler": {},
      "meta": {},
      "otaId": 1,
      "payment": "string",
      "paymentTerms": [
        {}
      ],
      "place": {},
      "placeId": 1,
      "priceCalculation": {},
      "product": {},
      "productId": 1,
      "reservationId": 1,
      "reservationUid": "string",
      "rows": [
        {}
      ],
      "status": "string",
      "timezone": "string",
      "total": 1,
      "type": "string",
      "typeActive": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accommodation` | object |  |
| `accommodationId` | number |  |
| `adminId` | number |  |
| `arrival` | date |  |
| `booker` | object |  |
| `categoryId` | number |  |
| `chainId` | number |  |
| `channel` | object |  |
| `channelId` | number |  |
| `contact` | object |  |
| `contactId` | number |  |
| `coTravelers` | object |  |
| `createDate` | date |  |
| `departure` | date |  |
| `draftId` | string |  |
| `groupId` | number |  |
| `id` | number |  |
| `invoices` | array<object> |  |
| `lastModified` | date |  |
| `mainTraveler` | object |  |
| `meta` | object |  |
| `otaId` | number |  |
| `payment` | string |  |
| `paymentTerms` | array<object> |  |
| `place` | object |  |
| `placeId` | number |  |
| `priceCalculation` | object |  |
| `product` | object |  |
| `productId` | number |  |
| `reservationId` | number |  |
| `reservationUid` | string |  |
| `rows` | array<object> |  |
| `status` | string |  |
| `timezone` | string |  |
| `total` | number |  |
| `type` | string |  |
| `typeActive` | boolean |  |

## Native endpoint

Through the native Starfish API, this operation is `POST /reservations` (base URL `https://api.camping.care/v21`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reservation.md) for the provider-specific parameters and requirements.

