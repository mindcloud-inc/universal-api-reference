# serviceminder.io: Find Appointment

Retrieves an appointment from ServiceMinder by ID.

```
GET https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/find-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a serviceminder.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/find-appointment?connectionId=$CONNECTION_ID&appointmentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appointmentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/find-appointment?${params}`, {
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
| `appointmentId` | number | yes | Appointment identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appointmentId": 1,
      "contactId": 1,
      "invoiceId": 1,
      "message": "string",
      "notificationOptions": [
        "string"
      ],
      "resultCode": 1,
      "serviceId": 1,
      "serviceName": "Ava Chen",
      "slots": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appointmentId` | number |  |
| `contactId` | number |  |
| `invoiceId` | number |  |
| `message` | string |  |
| `notificationOptions` | array<string> |  |
| `resultCode` | number |  |
| `serviceId` | number |  |
| `serviceName` | string |  |
| `slots` | array<object> |  |

## Native endpoint

Through the native serviceminder.io API, this operation is `POST /appointments/find` (base URL `https://serviceminder.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-appointment.md) for the provider-specific parameters and requirements.

