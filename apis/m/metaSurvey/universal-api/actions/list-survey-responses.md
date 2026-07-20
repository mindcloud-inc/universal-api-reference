# MetaSurvey: List Survey Responses



```
GET https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/list-survey-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MetaSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/list-survey-responses?connectionId=$CONNECTION_ID&surveyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/list-survey-responses?${params}`, {
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
| `surveyId` | string | yes | Survey whose responses should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "individualResults": [
        {}
      ],
      "results": [
        {}
      ],
      "summary": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `individualResults` | array<object> | Individual response rows. |
| `results` | array<object> | Aggregated question result rows. |
| `summary` | object | Survey response summary metrics. |

## Native endpoint

Through the native MetaSurvey API, this operation is `GET /admin/survey/:surveyId/responses` (base URL `https://api.getmetasurvey.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-survey-responses.md) for the provider-specific parameters and requirements.

