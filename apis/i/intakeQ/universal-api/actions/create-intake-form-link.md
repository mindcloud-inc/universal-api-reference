# IntakeQ: Create Intake Form Link

Creates an intake form link in IntakeQ.

```
POST https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/create-intake-form-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/create-intake-form-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/create-intake-form-link', {
  method: 'POST',
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
      "password": "string",
      "practitioner": "string",
      "practitionerName": "Ava Chen",
      "questionnaireName": "Ava Chen",
      "questions": [
        {}
      ],
      "status": "string",
      "url": "https://example.com"
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
| `password` | string |  |
| `practitioner` | string |  |
| `practitionerName` | string |  |
| `questionnaireName` | string |  |
| `questions` | array<object> |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native IntakeQ API, this operation is `POST /intakes/create` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-intake-form-link.md) for the provider-specific parameters and requirements.

