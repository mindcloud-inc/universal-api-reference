# IntakeQ: Create Appointment

Creates a new appointment in IntakeQ.

```
POST https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/create-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/create-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "practitionerId": "string",
  "clientId": "string",
  "serviceId": "string",
  "locationId": "string",
  "status": "string",
  "utcDateTime": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/create-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "practitionerId": "string",
    "clientId": "string",
    "serviceId": "string",
    "locationId": "string",
    "status": "string",
    "utcDateTime": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `practitionerId` | string | yes | The IntakeQ practitioner ID. |
| `clientId` | string | yes | The IntakeQ numeric client ID. |
| `serviceId` | string | yes | The IntakeQ service ID. |
| `locationId` | string | yes | The IntakeQ location ID. |
| `status` | string | yes | Appointment status. |
| `utcDateTime` | string | yes | Appointment start time as a Unix timestamp in milliseconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientDateOfBirth": "string",
      "clientEmail": "ava@example.com",
      "clientId": 1,
      "clientName": "Ava Chen",
      "clientPhone": "string",
      "dateCreated": 1,
      "duration": 1,
      "endDate": 1,
      "id": "string",
      "intakeId": "string",
      "locationId": "string",
      "locationName": "Ava Chen",
      "practitionerEmail": "ava@example.com",
      "practitionerName": "Ava Chen",
      "price": 1,
      "serviceId": "string",
      "serviceName": "Ava Chen",
      "startDate": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientDateOfBirth` | string |  |
| `clientEmail` | string |  |
| `clientId` | number |  |
| `clientName` | string |  |
| `clientPhone` | string |  |
| `dateCreated` | number |  |
| `duration` | number |  |
| `endDate` | number |  |
| `id` | string |  |
| `intakeId` | string |  |
| `locationId` | string |  |
| `locationName` | string |  |
| `practitionerEmail` | string |  |
| `practitionerName` | string |  |
| `price` | number |  |
| `serviceId` | string |  |
| `serviceName` | string |  |
| `startDate` | number |  |
| `status` | string |  |

## Native endpoint

Through the native IntakeQ API, this operation is `POST /appointments` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-appointment.md) for the provider-specific parameters and requirements.

