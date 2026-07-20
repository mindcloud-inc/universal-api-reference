# snapADDY: List Questionnaire Participants



```
GET https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/list-questionnaire-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a snapADDY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/list-questionnaire-participants?connectionId=$CONNECTION_ID&questionnaireId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "questionnaireId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/list-questionnaire-participants?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of participants to return |
| `page` | number | no | Page number |
| `filter` | string | no | Filter expression |

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
      "participantIds": [
        "string"
      ],
      "participants": [
        {}
      ],
      "participantsCount": 1,
      "questionnaires": [
        {}
      ],
      "questionOptions": [
        {}
      ],
      "questions": [
        {}
      ],
      "reports": [
        {}
      ],
      "reportsCount": 1
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
| `participantIds` | array<string> |  |
| `participants` | array<object> |  |
| `participantsCount` | number |  |
| `questionnaires` | array<object> |  |
| `questionOptions` | array<object> |  |
| `questions` | array<object> |  |
| `reports` | array<object> |  |
| `reportsCount` | number |  |

## Native endpoint

Through the native snapADDY API, this operation is `GET /visitreport/v1/backend/questionnaires/:questionnaireId/participants/all` (base URL `https://api.snapaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-questionnaire-participants.md) for the provider-specific parameters and requirements.

