# IntakeQ: Cancel Appointment

Cancels an appointment in IntakeQ.

```
DELETE https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/cancel-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/cancel-appointment?connectionId=$CONNECTION_ID&appointmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appointmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/cancel-appointment?${params}`, {
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
      "appointmentId": "string",
      "reason": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appointmentId` | string |  |
| `reason` | string |  |

## Native endpoint

Through the native IntakeQ API, this operation is `POST /appointments/cancellation` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-appointment.md) for the provider-specific parameters and requirements.

