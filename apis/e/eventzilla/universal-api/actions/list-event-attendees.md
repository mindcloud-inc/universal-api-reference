# Eventzilla: List Event Attendees

Retrieves attendees for an event from Eventzilla.

```
GET https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/list-event-attendees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventzilla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/list-event-attendees?connectionId=$CONNECTION_ID&eventId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/list-event-attendees?${params}`, {
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
| `eventId` | number | yes | The Eventzilla event identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "barCode": "string",
      "buyerFirstName": "Ava",
      "buyerLastName": "Chen",
      "email": "ava@example.com",
      "eventDate": "2026-05-07T12:00:00.000Z",
      "eventId": 1,
      "firstName": "Ava",
      "id": 1,
      "isAttended": true,
      "lastName": "Chen",
      "paymentType": "string",
      "questions": [
        {}
      ],
      "refno": "string",
      "ticketType": "string",
      "transactionAmount": 1,
      "transactionDate": "2026-05-07T12:00:00.000Z",
      "transactionStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `barCode` | string |  |
| `buyerFirstName` | string |  |
| `buyerLastName` | string |  |
| `email` | string |  |
| `eventDate` | date |  |
| `eventId` | number |  |
| `firstName` | string |  |
| `id` | number |  |
| `isAttended` | boolean |  |
| `lastName` | string |  |
| `paymentType` | string |  |
| `questions` | array<object> |  |
| `refno` | string |  |
| `ticketType` | string |  |
| `transactionAmount` | number |  |
| `transactionDate` | date |  |
| `transactionStatus` | string |  |

## Native endpoint

Through the native Eventzilla API, this operation is `GET /events/:eventid/attendees` (base URL `https://www.eventzillaapi.net/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-attendees.md) for the provider-specific parameters and requirements.

