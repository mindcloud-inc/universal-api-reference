# SurveyMethods: Get Survey



```
GET https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/get-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveyMethods `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/get-survey?connectionId=$CONNECTION_ID&surveyCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/get-survey?${params}`, {
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
| `surveyCode` | string | yes | SurveyMethods survey code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rowcount": 1,
      "status": "string",
      "survey": {
        "anonymous": "string",
        "attempts": "string",
        "closed_date": "2026-05-07T12:00:00.000Z",
        "code": "string",
        "collaborated": "string",
        "created_date": "2026-05-07T12:00:00.000Z",
        "default_publish_url": "https://example.com",
        "folder_name": "Ava Chen",
        "latest_launch_date": "2026-05-07T12:00:00.000Z",
        "page_count": 1,
        "question_count": 1,
        "response_count": 1,
        "ssl": {
          "published_reports": "string",
          "survey_link": "https://example.com"
        },
        "status": "string",
        "title": "string",
        "web_launch_url": "https://example.com",
        "width": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rowcount` | number |  |
| `status` | string |  |
| `survey` | object |  |
| `survey.anonymous` | string |  |
| `survey.attempts` | string |  |
| `survey.closed_date` | date |  |
| `survey.code` | string |  |
| `survey.collaborated` | string |  |
| `survey.created_date` | date |  |
| `survey.default_publish_url` | string |  |
| `survey.folder_name` | string |  |
| `survey.latest_launch_date` | date |  |
| `survey.page_count` | number |  |
| `survey.question_count` | number |  |
| `survey.response_count` | number |  |
| `survey.ssl` | object |  |
| `survey.ssl.published_reports` | string |  |
| `survey.ssl.survey_link` | string |  |
| `survey.status` | string |  |
| `survey.title` | string |  |
| `survey.web_launch_url` | string |  |
| `survey.width` | string |  |

## Native endpoint

Through the native SurveyMethods API, this operation is `GET /:loginId/:apiKey/surveys/:surveyCode/` (base URL `https://api.surveymethods.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey.md) for the provider-specific parameters and requirements.

