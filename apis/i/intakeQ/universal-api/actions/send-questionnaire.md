# IntakeQ: Send Questionnaire

Creates a questionnaire request in IntakeQ.

```
POST https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/send-questionnaire
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/send-questionnaire" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "questionnaireId": "string",
  "clientId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/send-questionnaire', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "questionnaireId": "string",
    "clientId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `questionnaireId` | string | yes | The IntakeQ questionnaire template ID. |
| `clientId` | string | yes | The IntakeQ numeric client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "intakeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `intakeId` | string |  |

## Native endpoint

Through the native IntakeQ API, this operation is `POST /intakes/send` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-questionnaire.md) for the provider-specific parameters and requirements.

