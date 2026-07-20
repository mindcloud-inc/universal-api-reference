# Bookafy: List Appointments

Retrieves appointments from Bookafy by date range.

```
GET https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/list-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookafy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/list-appointments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/list-appointments?${params}`, {
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
| `email` | string | no | Staff email address to scope the appointment list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {
        "appointment": [
          {
            "appointmentDate": "2026-05-07T12:00:00.000Z",
            "appointmentEndTime": "2026-05-07T12:00:00.000Z",
            "appointmentStartTime": "2026-05-07T12:00:00.000Z",
            "cancelToken": "string",
            "categoryId": 1,
            "customer": {
              "customerDetailHstore": {
                "email": "ava@example.com",
                "name": "Ava Chen"
              },
              "id": 1
            },
            "customerId": 1,
            "description": "string",
            "duration": "string",
            "id": 1,
            "isActive": true,
            "serviceId": 1,
            "timeZone": "string",
            "title": "string",
            "updateToken": "string",
            "user": {
              "email": "ava@example.com",
              "name": "Ava Chen"
            },
            "userId": 1
          }
        ],
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
| `response.appointment[].appointmentDate` | date | Appointment calendar date. |
| `response.appointment[].appointmentEndTime` | date | Appointment end timestamp. |
| `response.appointment[].appointmentStartTime` | date | Appointment start timestamp. |
| `response.appointment[].cancelToken` | string | Cancellation token for the appointment. |
| `response.appointment[].categoryId` | number | Appointment category ID. |
| `response.appointment[].customer.customerDetailHstore.email` | string | Customer email. |
| `response.appointment[].customer.customerDetailHstore.name` | string | Customer display name. |
| `response.appointment[].customer.id` | number | Customer ID nested in the appointment payload. |
| `response.appointment[].customerId` | number | Booked customer ID. |
| `response.appointment[].description` | string | Appointment description. |
| `response.appointment[].duration` | string | Appointment duration in minutes. |
| `response.appointment[].id` | number | Appointment ID. |
| `response.appointment[].isActive` | boolean | Whether the appointment is active. |
| `response.appointment[].serviceId` | number | Booked service ID. |
| `response.appointment[].timeZone` | string | Appointment time zone label. |
| `response.appointment[].title` | string | Appointment title. |
| `response.appointment[].updateToken` | string | Update token for the appointment. |
| `response.appointment[].user.email` | string | Assigned staff member email. |
| `response.appointment[].user.name` | string | Assigned staff member name. |
| `response.appointment[].userId` | number | Assigned staff member ID. |
| `response.message` | string | Bookafy status message for the list request. |

## Native endpoint

Through the native Bookafy API, this operation is `GET /appointments` (base URL `https://app.bookafy.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-appointments.md) for the provider-specific parameters and requirements.

