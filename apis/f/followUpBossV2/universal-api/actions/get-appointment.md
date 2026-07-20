# Follow Up Boss: Get Appointment

Retrieves an appointment from Follow Up Boss.

```
GET https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-appointment?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-appointment?${params}`, {
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
| `id` | string | yes | The appointment ID. |

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

Through the native Follow Up Boss API, this operation is `GET appointments/:id` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-appointment.md) for the provider-specific parameters and requirements.

