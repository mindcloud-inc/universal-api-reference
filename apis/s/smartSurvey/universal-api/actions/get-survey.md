# SmartSurvey: Get Survey

Retrieves a survey from your SmartSurvey account.

```
GET https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey?connectionId=$CONNECTION_ID&surveyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey?${params}`, {
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
| `surveyId` | number | yes | The survey id of the survey to fetch |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `translationId` | number | no | The id of the translation you want the details in or 0 for the default Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date_created": "2026-05-07T12:00:00.000Z",
      "date_modified": "2026-05-07T12:00:00.000Z",
      "href": "string",
      "href_links": "https://example.com",
      "href_responses": "string",
      "id": 1,
      "nickname": "Ava Chen",
      "page_count": 1,
      "question_count": 1,
      "responses": 1,
      "status": "string",
      "survey_url": "https://example.com",
      "theme_id": 1,
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date_created` | date |  |
| `date_modified` | date |  |
| `href` | string |  |
| `href_links` | string |  |
| `href_responses` | string |  |
| `id` | number |  |
| `nickname` | string |  |
| `page_count` | number |  |
| `question_count` | number |  |
| `responses` | number |  |
| `status` | string |  |
| `survey_url` | string |  |
| `theme_id` | number |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native SmartSurvey API, this operation is `GET /surveys/{surveyId}` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey.md) for the provider-specific parameters and requirements.

