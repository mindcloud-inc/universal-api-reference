# Bookafy: Update Appointment

Updates an appointment in Bookafy.

```
PUT https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/update-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookafy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/update-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/update-appointment', {
  method: 'PUT',
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
| `appointmentDate` | string | no | Appointment date in YYYY-MM-DD format. |
| `appointmentEndTime` | string | no | Appointment end time in Bookafy's displayed time format, for example 12:15 PM. |
| `appointmentStartTime` | string | no | Appointment start time in Bookafy's displayed time format, for example 12:00 PM. |
| `categoryId` | string | no | Bookafy category ID for the appointment. |
| `customerEmail` | string | no | Customer email address on the appointment. |
| `customerName` | string | no | Customer full name on the appointment. |
| `customerPhone` | string | no | Customer phone number on the appointment. |
| `description` | string | no | Appointment description value sent to Bookafy. |
| `duration` | string | no | Appointment duration in minutes. |
| `id` | string | no | Bookafy appointment ID to update. |
| `serviceId` | string | no | Bookafy service ID for the appointment. |
| `timeZone` | string | no | Bookafy time zone label, for example Central Time (US & Canada). |
| `title` | string | no | Appointment title value sent to Bookafy. |
| `userId` | string | no | Bookafy staff user ID that owns the appointment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {
        "appointment": {
          "appointmentDate": "2026-05-07T12:00:00.000Z",
          "appointmentEndTime": "2026-05-07T12:00:00.000Z",
          "appointmentStartTime": "2026-05-07T12:00:00.000Z",
          "cancelToken": "string",
          "category": {
            "categoryId": 1,
            "categoryName": "Ava Chen"
          },
          "createdAt": "2026-05-07T12:00:00.000Z",
          "customerId": 1,
          "description": "string",
          "duration": "string",
          "id": 1,
          "isActive": true,
          "service": {
            "serviceId": 1,
            "serviceName": "Ava Chen"
          },
          "title": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "updateToken": "string",
          "userId": 1
        },
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response.appointment.appointmentDate` | date | Appointment calendar date. |
| `response.appointment.appointmentEndTime` | date | Appointment end timestamp. |
| `response.appointment.appointmentStartTime` | date | Appointment start timestamp. |
| `response.appointment.cancelToken` | string | Cancellation token for the appointment. |
| `response.appointment.category.categoryId` | number | Appointment category ID. |
| `response.appointment.category.categoryName` | string | Appointment category name. |
| `response.appointment.createdAt` | date | Appointment creation timestamp. |
| `response.appointment.customerId` | number | Booked customer ID. |
| `response.appointment.description` | string | Appointment description. |
| `response.appointment.duration` | string | Appointment duration in minutes. |
| `response.appointment.id` | number | Appointment ID. |
| `response.appointment.isActive` | boolean | Whether the appointment is active. |
| `response.appointment.service.serviceId` | number | Booked service ID. |
| `response.appointment.service.serviceName` | string | Booked service name. |
| `response.appointment.title` | string | Appointment title. |
| `response.appointment.updatedAt` | date | Appointment update timestamp. |
| `response.appointment.updateToken` | string | Update token for the appointment. |
| `response.appointment.userId` | number | Assigned staff member ID. |
| `response.message` | string | Bookafy status message for the update request. |

## Native endpoint

Through the native Bookafy API, this operation is `PUT /appointments/:id` (base URL `https://app.bookafy.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-appointment.md) for the provider-specific parameters and requirements.

