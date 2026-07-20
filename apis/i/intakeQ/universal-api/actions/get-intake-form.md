# IntakeQ: Get Intake Form

Retrieves an intake form from IntakeQ.

```
GET https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/get-intake-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/get-intake-form?connectionId=$CONNECTION_ID&intakeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "intakeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/get-intake-form?${params}`, {
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
| `intakeId` | string | yes | The IntakeQ intake form ID. |

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
      "consentForms": [
        {}
      ],
      "dateCreated": 1,
      "dateSubmitted": 1,
      "externalClientId": "string",
      "id": "string",
      "practitioner": "string",
      "practitionerName": "Ava Chen",
      "questionnaireName": "Ava Chen",
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
| `consentForms` | array<object> |  |
| `dateCreated` | number |  |
| `dateSubmitted` | number |  |
| `externalClientId` | string |  |
| `id` | string |  |
| `practitioner` | string |  |
| `practitionerName` | string |  |
| `questionnaireName` | string |  |
| `questions` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native IntakeQ API, this operation is `GET /intakes/{intakeId}` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-intake-form.md) for the provider-specific parameters and requirements.

