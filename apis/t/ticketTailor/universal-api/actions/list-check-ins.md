# Ticket Tailor: List Check Ins

Retrieves box office check-ins from Ticket Tailor.

```
GET https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-check-ins
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticket Tailor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-check-ins?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-check-ins?${params}`, {
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
      "checkInAt": 1,
      "createdAt": 1,
      "eventId": "string",
      "id": "string",
      "issuedTicketId": "string",
      "localUniqueId": "string",
      "object": "string",
      "quantity": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkInAt` | number | Timestamp of when the ticket is checked in or out |
| `createdAt` | number | Check in creation timestamp |
| `eventId` | string | The ID of the associated event |
| `id` | string |  |
| `issuedTicketId` | string | The ID of the associated ticket that is to be checked in or out |
| `localUniqueId` | string | The optional unique ID that safegards from accidentally checking in multiple times |
| `object` | string |  |
| `quantity` | number | in=1, out=-1 |

## Native endpoint

Through the native Ticket Tailor API, this operation is `GET /v1/check_ins` (base URL `https://api.tickettailor.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-check-ins.md) for the provider-specific parameters and requirements.

