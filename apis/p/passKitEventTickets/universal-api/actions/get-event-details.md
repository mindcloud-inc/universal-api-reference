# PassKit Event Tickets: Get Event Details

Retrieves an event by start date and venue from PassKit.

```
GET https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-event-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Event Tickets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-event-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-event-details?${params}`, {
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
| `productionId` | string | no | Filter event details by production id. |
| `productionUid` | string | no | Filter event details by production uid. |
| `scheduledStartDate` | string | no | Filter event details by scheduled start date. |
| `venueId` | string | no | Filter event details by venue id. |
| `venueUid` | string | no | Filter event details by venue uid. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "eventId": "string",
      "id": "string",
      "name": "Ava Chen",
      "scheduledStartDate": "string",
      "uid": "string",
      "venueId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eventId` | string |  |
| `id` | string |  |
| `name` | string |  |
| `scheduledStartDate` | string |  |
| `uid` | string |  |
| `venueId` | string |  |

## Native endpoint

Through the native PassKit Event Tickets API, this operation is `GET /eventTickets/event/details` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-details.md) for the provider-specific parameters and requirements.

