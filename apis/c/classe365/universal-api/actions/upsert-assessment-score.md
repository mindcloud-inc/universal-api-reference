# Classe365: Upsert Assessment Score

Creates or updates an assessment score in Classe365.

```
POST https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-assessment-score
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-assessment-score" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-assessment-score', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `acds_id` | string | no | Academic session id. |
| `assessment_id` | string | no | Assessment id. |
| `score_data` | string | no | JSON map of student scores. |
| `subject_id` | string | no | Subject id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assessmentId": 1,
      "score": "string",
      "studentId": 1,
      "subjectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assessmentId` | number |  |
| `score` | string |  |
| `studentId` | number |  |
| `subjectId` | number |  |

## Native endpoint

Through the native Classe365 API, this operation is `POST /rest/saveAssessmentScore` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-assessment-score.md) for the provider-specific parameters and requirements.

