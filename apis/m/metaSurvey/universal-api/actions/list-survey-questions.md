# MetaSurvey: List Survey Questions



```
GET https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/list-survey-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MetaSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/list-survey-questions?connectionId=$CONNECTION_ID&surveyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/list-survey-questions?${params}`, {
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
| `surveyId` | string | yes | Survey whose questions should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "rows": [
        {}
      ],
      "show_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of questions returned. |
| `rows` | array<object> | Survey question rows. |
| `show_count` | number | Visible question count. |

## Native endpoint

Through the native MetaSurvey API, this operation is `GET /admin/survey/:surveyId/questions` (base URL `https://api.getmetasurvey.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-survey-questions.md) for the provider-specific parameters and requirements.

