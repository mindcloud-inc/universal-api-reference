# IntakeQ: Resend Questionnaire

Resends a questionnaire from IntakeQ.

```
PUT https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/resend-questionnaire
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/resend-questionnaire" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "intakeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/resend-questionnaire', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "intakeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `intakeId` | string | yes | The IntakeQ intake form ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deliveryMethod": "string",
      "intakeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deliveryMethod` | string |  |
| `intakeId` | string |  |

## Native endpoint

Through the native IntakeQ API, this operation is `POST /intakes/resend` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resend-questionnaire.md) for the provider-specific parameters and requirements.

