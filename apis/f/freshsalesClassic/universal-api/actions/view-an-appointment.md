# Freshsales Classic: View an Appointment

Retrieves an appointment from Freshsales Classic.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/view-an-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/view-an-appointment?connectionId=$CONNECTION_ID&appointmentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appointmentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/view-an-appointment?${params}`, {
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
| `appointmentId` | number | yes | The appointment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appointmentAttendeeIds": [
        1
      ],
      "createdAt": "string",
      "createrId": 1,
      "description": "string",
      "endDate": "string",
      "fromDate": "string",
      "hasMultipleEmails": true,
      "id": 1,
      "isAllday": true,
      "location": "string",
      "outcomeId": 1,
      "provider": "string",
      "targetables": [
        {}
      ],
      "targetablesWithEmail": [
        {}
      ],
      "timeZone": "string",
      "title": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appointmentAttendeeIds` | array<number> |  |
| `createdAt` | string |  |
| `createrId` | number |  |
| `description` | string |  |
| `endDate` | string |  |
| `fromDate` | string |  |
| `hasMultipleEmails` | boolean |  |
| `id` | number |  |
| `isAllday` | boolean |  |
| `location` | string |  |
| `outcomeId` | number |  |
| `provider` | string |  |
| `targetables` | array<object> |  |
| `targetablesWithEmail` | array<object> |  |
| `timeZone` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /appointments/:appointmentId` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-an-appointment.md) for the provider-specific parameters and requirements.

