# Starfish: Get Reservation

Retrieves a specific reservation from Starfish.

```
GET https://connect.mindcloud.co/v1/universal/starfish/latest/actions/get-reservation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starfish `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/get-reservation?connectionId=$CONNECTION_ID&reservationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reservationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starfish/latest/actions/get-reservation?${params}`, {
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
| `reservationId` | number | yes | Reservation ID. |

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
      "meta": [
        {}
      ],
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
| `meta` | array<object> |  |
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

Through the native Starfish API, this operation is `GET /reservations/:id` (base URL `https://api.camping.care/v21`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reservation.md) for the provider-specific parameters and requirements.

