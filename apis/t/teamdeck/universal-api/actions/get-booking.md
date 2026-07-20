# Teamdeck: Get Booking

Retrieves a booking from your Teamdeck organization.

```
GET https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/get-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamdeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/get-booking?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/get-booking?${params}`, {
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
| `id` | number | yes | The Teamdeck booking ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creatorResourceId": 1,
      "description": "string",
      "editorResourceId": 1,
      "endDate": "string",
      "externalId": "string",
      "holidaysBooking": true,
      "hours": 1,
      "id": 1,
      "minutes": 1,
      "percentage": 1,
      "projectId": 1,
      "resourceId": 1,
      "rrule": "string",
      "startDate": "string",
      "vacationsBooking": true,
      "weekendBooking": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creatorResourceId` | number |  |
| `description` | string |  |
| `editorResourceId` | number |  |
| `endDate` | string |  |
| `externalId` | string |  |
| `holidaysBooking` | boolean |  |
| `hours` | number |  |
| `id` | number |  |
| `minutes` | number |  |
| `percentage` | number |  |
| `projectId` | number |  |
| `resourceId` | number |  |
| `rrule` | string |  |
| `startDate` | string |  |
| `vacationsBooking` | boolean |  |
| `weekendBooking` | boolean |  |

## Native endpoint

Through the native Teamdeck API, this operation is `GET /bookings/:id` (base URL `https://api.teamdeck.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking.md) for the provider-specific parameters and requirements.

