# Teamdeck: Update Booking

Updates an existing booking in Teamdeck.

```
PUT https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/update-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamdeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/update-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "resourceId": 1,
  "projectId": 1,
  "minutes": 1,
  "startDate": "string",
  "endDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/update-booking', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "resourceId": 1,
    "projectId": 1,
    "minutes": 1,
    "startDate": "string",
    "endDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The Teamdeck booking ID. |
| `resourceId` | number | yes |  |
| `projectId` | number | yes |  |
| `minutes` | number | yes |  |
| `percentage` | number | no |  |
| `weekendBooking` | boolean | no |  |
| `holidaysBooking` | boolean | no |  |
| `vacationsBooking` | boolean | no |  |
| `rrule` | string | no |  |
| `description` | string | no |  |
| `externalId` | string | no |  |
| `startDate` | string | yes |  |
| `endDate` | string | yes |  |
| `creatorResourceId` | number | no |  |
| `editorResourceId` | number | no |  |

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

Through the native Teamdeck API, this operation is `PUT /bookings/:id` (base URL `https://api.teamdeck.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-booking.md) for the provider-specific parameters and requirements.

