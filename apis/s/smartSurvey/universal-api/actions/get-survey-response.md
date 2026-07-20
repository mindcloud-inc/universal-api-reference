# SmartSurvey: Get Survey Response

Retrieves a survey response from SmartSurvey.

```
GET https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey-response?connectionId=$CONNECTION_ID&surveyId=1&responseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "1",
  "responseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/get-survey-response?${params}`, {
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
| `surveyId` | number | yes | The survey id whose Response you are querying |
| `responseId` | number | yes | The Response id that you are querying |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `translationId` | number | no | The translation id to load - defaults to English Default: `1`. |
| `includeLabels` | boolean | no | Whether to include labels in the response - can increase the size of the payload significantly Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_data": {
        "name": "Ava Chen",
        "value": "string"
      },
      "contact_email": "ava@example.com",
      "contact_invitation_id": 1,
      "contact_name": "Ava Chen",
      "country": "string",
      "current_page_id": 1,
      "date_ended": "2026-05-07T12:00:00.000Z",
      "date_modified": "2026-05-07T12:00:00.000Z",
      "date_started": "2026-05-07T12:00:00.000Z",
      "edit_url": "https://example.com",
      "entry_url": "https://example.com",
      "href": "string",
      "id": 1,
      "ip_address": "string",
      "manual_entry": true,
      "page_path": "string",
      "pages": [
        {}
      ],
      "referer_url": "https://example.com",
      "saved": true,
      "saved_continue_url": "https://example.com",
      "saved_email": "ava@example.com",
      "saved_name": "Ava Chen",
      "status": "string",
      "survey_id": 1,
      "total_score": 1,
      "tracking_link_id": 1,
      "translation_id": 1,
      "unique_id": "string",
      "user_agent": "string",
      "variables": {
        "id": 1,
        "label": "string",
        "name": "Ava Chen",
        "value": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_data` | array<object> |  |
| `contact_data.name` | string |  |
| `contact_data.value` | string |  |
| `contact_email` | string |  |
| `contact_invitation_id` | number |  |
| `contact_name` | string |  |
| `country` | string |  |
| `current_page_id` | number |  |
| `date_ended` | date |  |
| `date_modified` | date |  |
| `date_started` | date |  |
| `edit_url` | string |  |
| `entry_url` | string |  |
| `href` | string |  |
| `id` | number |  |
| `ip_address` | string |  |
| `manual_entry` | boolean |  |
| `page_path` | string |  |
| `pages` | array<object> |  |
| `referer_url` | string |  |
| `saved` | boolean |  |
| `saved_continue_url` | string |  |
| `saved_email` | string |  |
| `saved_name` | string |  |
| `status` | string |  |
| `survey_id` | number |  |
| `total_score` | number |  |
| `tracking_link_id` | number |  |
| `translation_id` | number |  |
| `unique_id` | string |  |
| `user_agent` | string |  |
| `variables` | array<object> |  |
| `variables.id` | number |  |
| `variables.label` | string |  |
| `variables.name` | string |  |
| `variables.value` | string |  |

## Native endpoint

Through the native SmartSurvey API, this operation is `GET /surveys/{surveyId}/responses/{responseId}` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey-response.md) for the provider-specific parameters and requirements.

