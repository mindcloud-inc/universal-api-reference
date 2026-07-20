# IntakeQ: Get Treatment Note

Retrieves a treatment note from IntakeQ.

```
GET https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/get-treatment-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/get-treatment-note?connectionId=$CONNECTION_ID&noteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "noteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/get-treatment-note?${params}`, {
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
| `noteId` | string | yes | The IntakeQ treatment note ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appointmentId": "string",
      "clientEmail": "ava@example.com",
      "clientId": 1,
      "clientName": "Ava Chen",
      "date": 1,
      "id": "string",
      "noteName": "Ava Chen",
      "practitionerEmail": "ava@example.com",
      "practitionerId": "string",
      "practitionerName": "Ava Chen",
      "questions": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appointmentId` | string |  |
| `clientEmail` | string |  |
| `clientId` | number |  |
| `clientName` | string |  |
| `date` | number |  |
| `id` | string |  |
| `noteName` | string |  |
| `practitionerEmail` | string |  |
| `practitionerId` | string |  |
| `practitionerName` | string |  |
| `questions` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native IntakeQ API, this operation is `GET /notes/{noteId}` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-treatment-note.md) for the provider-specific parameters and requirements.

