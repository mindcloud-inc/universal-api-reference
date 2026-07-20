# Follow Up Boss: Create Appointment

Creates a new appointment in Follow Up Boss.

```
POST https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/create-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/create-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/create-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invitees[].personId` | number | no |  |
| `invitees[].userId` | number | no |  |
| `title` | string | no |  |
| `description` | string | no |  |
| `start` | date | no |  |
| `end` | date | no |  |
| `timezone` | string | no |  |
| `location` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allDay": true,
      "created": "2026-05-07T12:00:00.000Z",
      "createdById": 1,
      "description": "string",
      "detailsVisible": true,
      "end": "2026-05-07T12:00:00.000Z",
      "externalCalendarId": "string",
      "externalEventLink": "https://example.com",
      "id": 1,
      "invitees": [
        {}
      ],
      "isDeletable": true,
      "isEditable": true,
      "location": "string",
      "originFub": true,
      "outcome": "string",
      "outcomeId": 1,
      "start": "2026-05-07T12:00:00.000Z",
      "timezone": "string",
      "title": "string",
      "type": "string",
      "typeId": 1,
      "updated": "2026-05-07T12:00:00.000Z",
      "updatedById": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allDay` | boolean |  |
| `created` | date |  |
| `createdById` | number |  |
| `description` | string |  |
| `detailsVisible` | boolean |  |
| `end` | date |  |
| `externalCalendarId` | string |  |
| `externalEventLink` | string |  |
| `id` | number |  |
| `invitees` | array<object> |  |
| `isDeletable` | boolean |  |
| `isEditable` | boolean |  |
| `location` | string |  |
| `originFub` | boolean |  |
| `outcome` | string |  |
| `outcomeId` | number |  |
| `start` | date |  |
| `timezone` | string |  |
| `title` | string |  |
| `type` | string |  |
| `typeId` | number |  |
| `updated` | date |  |
| `updatedById` | number |  |

## Native endpoint

Through the native Follow Up Boss API, this operation is `POST appointments` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-appointment.md) for the provider-specific parameters and requirements.

