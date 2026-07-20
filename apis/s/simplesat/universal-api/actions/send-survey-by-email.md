# Simplesat: Send Survey by Email

Sends a survey by email from Simplesat.

```
POST https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/send-survey-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplesat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/send-survey-by-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/send-survey-by-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyToken": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyToken` | string | yes | The token of the survey to send |
| `customer` | object | no |  |
| `teamMember` | object | no |  |
| `ticket` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "detail": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `detail` | string |  |

## Native endpoint

Through the native Simplesat API, this operation is `POST /api/v1/surveys/:survey_token/email` (base URL `https://api.simplesat.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-survey-by-email.md) for the provider-specific parameters and requirements.

