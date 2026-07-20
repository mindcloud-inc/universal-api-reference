# IntakeQ: Get Appointment

Retrieves an appointment from IntakeQ.

```
GET https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/get-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/get-appointment?connectionId=$CONNECTION_ID&appointmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appointmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/get-appointment?${params}`, {
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
| `appointmentId` | string | yes | The IntakeQ appointment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalClients": [
        {}
      ],
      "cancellationDate": "string",
      "clientDateOfBirth": "string",
      "clientEmail": "ava@example.com",
      "clientId": 1,
      "clientName": "Ava Chen",
      "clientPhone": "string",
      "customFields": [
        {}
      ],
      "dateCreated": 1,
      "duration": 1,
      "endDate": 1,
      "id": "string",
      "intakeId": "string",
      "invoiceId": "string",
      "invoiceNumber": 1,
      "lastModified": 1,
      "locationId": "string",
      "locationName": "Ava Chen",
      "practitionerEmail": "ava@example.com",
      "practitionerName": "Ava Chen",
      "price": 1,
      "serviceId": "string",
      "serviceName": "Ava Chen",
      "startDate": 1,
      "status": "string",
      "telehealthInfo": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalClients` | array<object> |  |
| `cancellationDate` | string |  |
| `clientDateOfBirth` | string |  |
| `clientEmail` | string |  |
| `clientId` | number |  |
| `clientName` | string |  |
| `clientPhone` | string |  |
| `customFields` | array<object> |  |
| `dateCreated` | number |  |
| `duration` | number |  |
| `endDate` | number |  |
| `id` | string |  |
| `intakeId` | string |  |
| `invoiceId` | string |  |
| `invoiceNumber` | number |  |
| `lastModified` | number |  |
| `locationId` | string |  |
| `locationName` | string |  |
| `practitionerEmail` | string |  |
| `practitionerName` | string |  |
| `price` | number |  |
| `serviceId` | string |  |
| `serviceName` | string |  |
| `startDate` | number |  |
| `status` | string |  |
| `telehealthInfo` | object |  |

## Native endpoint

Through the native IntakeQ API, this operation is `GET /appointments/{appointmentId}` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-appointment.md) for the provider-specific parameters and requirements.

