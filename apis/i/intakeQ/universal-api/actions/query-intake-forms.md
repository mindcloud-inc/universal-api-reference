# IntakeQ: Query Intake Forms

Retrieves intake forms from IntakeQ.

```
GET https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/query-intake-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/query-intake-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/query-intake-forms?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "clientEmail": "ava@example.com",
      "clientId": 1,
      "clientName": "Ava Chen",
      "dateCreated": 1,
      "dateSubmitted": 1,
      "externalClientId": "string",
      "id": "string",
      "practitioner": "string",
      "practitionerName": "Ava Chen",
      "questionnaireId": "string",
      "questionnaireName": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientEmail` | string |  |
| `clientId` | number |  |
| `clientName` | string |  |
| `dateCreated` | number |  |
| `dateSubmitted` | number |  |
| `externalClientId` | string |  |
| `id` | string |  |
| `practitioner` | string |  |
| `practitionerName` | string |  |
| `questionnaireId` | string |  |
| `questionnaireName` | string |  |
| `status` | string |  |

## Native endpoint

Through the native IntakeQ API, this operation is `GET /intakes/summary` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-intake-forms.md) for the provider-specific parameters and requirements.

