# SmartSurvey: List Survey Responses

Retrieves survey responses from a SmartSurvey survey.

```
GET https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-survey-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-survey-responses?connectionId=$CONNECTION_ID&limit=25&offset=0&surveyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "surveyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-survey-responses?${params}`, {
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
| `surveyId` | number | yes | The survey id whose Responses you are querying |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `completed` | number | no | Whether to only include completed responses Default: `1`. |
| `translationId` | number | no | The translation for the results - defaults to English Default: `1`. |
| `since` | number | no | Unix timestamp to filter results after a date/time Default: `0`. |
| `until` | number | no | Unix timestamp to filter results before a date/time Default: `0`. |
| `filterId` | number | no | Optional filter id for the results Default: `0`. |
| `trackingLinkId` | number | no | Tracking link id to filter results Default: `0`. |
| `uniqueId` | string | no | Filter on the user unique id |
| `includeLabels` | boolean | no | Whether to include question and page labels (reduces the size of the response) Default: `false`. |

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

Through the native SmartSurvey API, this operation is `GET /surveys/{surveyId}/responses` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-survey-responses.md) for the provider-specific parameters and requirements.

