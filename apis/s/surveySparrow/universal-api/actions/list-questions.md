# SurveySparrow: List Questions

Retrieves survey questions from SurveySparrow.

```
GET https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-questions?connectionId=$CONNECTION_ID&limit=25&offset=0&surveyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "surveyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-questions?${params}`, {
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
| `surveyId` | number | yes | ID of the survey. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tagName` | string | no | Filter questions by tag name. |
| `languageLabel` | string | no | Filter questions by language label. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annotations": [
        "string"
      ],
      "choices": [
        "string"
      ],
      "created_at": {},
      "id": 1,
      "is_required": true,
      "multiple_answers": true,
      "parent_question_id": "string",
      "position": "string",
      "properties": {},
      "rtxt": "string",
      "scale_points": [
        "string"
      ],
      "section": {},
      "tags": [
        "string"
      ],
      "type": "string",
      "updated_at": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annotations` | array<string> |  |
| `choices` | array<string> |  |
| `created_at` | object |  |
| `id` | number |  |
| `is_required` | boolean |  |
| `multiple_answers` | boolean |  |
| `parent_question_id` | string |  |
| `position` | string |  |
| `properties` | object |  |
| `rtxt` | string |  |
| `scale_points` | array<string> |  |
| `section` | object |  |
| `tags` | array<string> |  |
| `type` | string |  |
| `updated_at` | object |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `GET /questions` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-questions.md) for the provider-specific parameters and requirements.

