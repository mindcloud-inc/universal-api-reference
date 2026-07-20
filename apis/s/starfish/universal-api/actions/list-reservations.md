# Starfish: List Reservations

Retrieves a list of reservations from Starfish.

```
GET https://connect.mindcloud.co/v1/universal/starfish/latest/actions/list-reservations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starfish `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/list-reservations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starfish/latest/actions/list-reservations?${params}`, {
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
| `limit` | number | no | Maximum number of reservations to return. |
| `offset` | number | no | Number of reservations to skip before returning results. |
| `count` | boolean | no | Return the total reservation count instead of rows when true. |
| `orderBy` | string | no | Sort reservations by id, last_modified, arrival, or departure. |
| `order` | string | no | Sort direction: asc or desc. |
| `status` | string | no | Filter reservations by status. |
| `arrival` | date | no | Filter reservations by arrival date or date range. |
| `departure` | date | no | Filter reservations by departure date or date range. |
| `accommodationId` | number | no | Return only reservations for a specific accommodation. |
| `contactId` | number | no | Return only reservations for a specific contact. |

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
      "lastModifiedSearch": "2026-05-07T12:00:00.000Z",
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
      "total": "string",
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
| `lastModifiedSearch` | date |  |
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
| `total` | string |  |
| `type` | string |  |
| `typeActive` | boolean |  |

## Native endpoint

Through the native Starfish API, this operation is `GET /reservations` (base URL `https://api.camping.care/v21`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-reservations.md) for the provider-specific parameters and requirements.

