# Ticket Tailor: List Holds

Retrieves holds from Ticket Tailor.

```
GET https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-holds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticket Tailor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-holds?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-holds?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": {
        "date": "string",
        "formatted": "string",
        "iso": "string",
        "time": "string",
        "timezone": "string",
        "unix": 1
      },
      "eventId": "string",
      "id": "string",
      "note": "string",
      "object": "string",
      "quantities": [
        {
          "quantity": 1,
          "ticketTypeId": "string"
        }
      ],
      "totalOnHold": 1,
      "updatedAt": {
        "date": "string",
        "formatted": "string",
        "iso": "string",
        "time": "string",
        "timezone": "string",
        "unix": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | object |  |
| `createdAt.date` | string | ISO-8601 date for the created timestamp of the hold |
| `createdAt.formatted` | string | A formatted date string for the created timestamp of the hold |
| `createdAt.iso` | string | ISO-8601 date and time for the created timestamp of the hold |
| `createdAt.time` | string | Time of the created timestamp of the hold |
| `createdAt.timezone` | string | Timezone offset for the created timestamp of the hold |
| `createdAt.unix` | number | Unix timestamp for when the hold was created |
| `eventId` | string | ID of the event that the hold belongs to |
| `id` | string | A unque identifier for the hold |
| `note` | string | A note for the hold |
| `object` | string |  |
| `quantities` | array<object> | Hold quantities for each of the associated ticket type ID |
| `quantities[].quantity` | number | Number of held tickets of this type |
| `quantities[].ticketTypeId` | string | Ticket type ID |
| `totalOnHold` | number | Total number of tickets on hold |
| `updatedAt` | object |  |
| `updatedAt.date` | string | ISO-8601 date for the updated timestamp of the hold |
| `updatedAt.formatted` | string | A formatted date string for the updated timestamp of the hold |
| `updatedAt.iso` | string | ISO-8601 date and time for the updated timestamp of the hold |
| `updatedAt.time` | string | Time of the updated timestamp of the hold |
| `updatedAt.timezone` | string | Timezone offset for the updated timestamp of the hold |
| `updatedAt.unix` | number | Unix timestamp for when the hold was updated |

## Native endpoint

Through the native Ticket Tailor API, this operation is `GET /v1/holds` (base URL `https://api.tickettailor.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-holds.md) for the provider-specific parameters and requirements.

