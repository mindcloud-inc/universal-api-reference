# Ticket Generator: Get Event Details

Retrieves active event details and ticket categories from Ticket Generator.

```
GET https://connect.mindcloud.co/v1/universal/ticketGenerator/latest/actions/get-event-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticket Generator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketGenerator/latest/actions/get-event-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketGenerator/latest/actions/get-event-details?${params}`, {
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
      "description": "string",
      "endDateTime": "string",
      "eventId": "string",
      "eventName": "Ava Chen",
      "eventType": "string",
      "note": "string",
      "seatsIoVenueData": {},
      "startDateTime": "string",
      "ticketCategories": [
        {}
      ],
      "timezone": "string",
      "venue": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `endDateTime` | string |  |
| `eventId` | string |  |
| `eventName` | string |  |
| `eventType` | string |  |
| `note` | string |  |
| `seatsIoVenueData` | object |  |
| `startDateTime` | string |  |
| `ticketCategories` | array<object> |  |
| `timezone` | string |  |
| `venue` | string |  |

## Native endpoint

Through the native Ticket Generator API, this operation is `GET v1/event/details/` (base URL `https://apis.ticket-generator.com/client`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-details.md) for the provider-specific parameters and requirements.

