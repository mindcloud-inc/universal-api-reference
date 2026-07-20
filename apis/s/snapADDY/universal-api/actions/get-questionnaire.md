# snapADDY: Get Questionnaire



```
GET https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-questionnaire
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a snapADDY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-questionnaire?connectionId=$CONNECTION_ID&questionnaireId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "questionnaireId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-questionnaire?${params}`, {
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
| `questionnaireId` | string | yes | Questionnaire identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answerOptions": [
        {}
      ],
      "answers": [
        {}
      ],
      "groups": [
        {}
      ],
      "participants": [
        {}
      ],
      "questionnaires": [
        {}
      ],
      "questionOptionAttachments": [
        {}
      ],
      "questionOptions": [
        {}
      ],
      "questions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answerOptions` | array<object> |  |
| `answers` | array<object> |  |
| `groups` | array<object> |  |
| `participants` | array<object> |  |
| `questionnaires` | array<object> |  |
| `questionOptionAttachments` | array<object> |  |
| `questionOptions` | array<object> |  |
| `questions` | array<object> |  |

## Native endpoint

Through the native snapADDY API, this operation is `GET /visitreport/v1/backend/questionnaires/:questionnaireId` (base URL `https://api.snapaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-questionnaire.md) for the provider-specific parameters and requirements.

