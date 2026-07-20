# mfr Field Service Management: Create Appointment

Creates an appointment in mfr Field Service Management.

```
POST https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/create-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mfr Field Service Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/create-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "state": "string",
  "startDateTime": "2026-05-07T12:00:00.000Z",
  "endDateTime": "2026-05-07T12:00:00.000Z",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/create-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "state": "string",
    "startDateTime": "2026-05-07T12:00:00.000Z",
    "endDateTime": "2026-05-07T12:00:00.000Z",
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Appointment type. |
| `state` | string | yes | Appointment state. |
| `startDateTime` | date | yes | Appointment start timestamp. |
| `endDateTime` | date | yes | Appointment end timestamp. |
| `contactId` | string | yes | Primary contact ID for the appointment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appointmentType": "string",
      "contactId": 1,
      "endDateTime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "serviceRequestId": 1,
      "startDateTime": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appointmentType` | string |  |
| `contactId` | number |  |
| `endDateTime` | date |  |
| `id` | number |  |
| `serviceRequestId` | number |  |
| `startDateTime` | date |  |
| `state` | string |  |
| `type` | string |  |

## Native endpoint

Through the native mfr Field Service Management API, this operation is `POST Appointments` (base URL `https://portal.mobilefieldreport.com/odata`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-appointment.md) for the provider-specific parameters and requirements.

