# SurveySparrow: Get Survey

Retrieves a survey from SurveySparrow.

```
GET https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/get-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/get-survey?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/get-survey?${params}`, {
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
| `id` | number | yes | ID of the survey. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "created_at": {},
      "id": 1,
      "name": "Ava Chen",
      "response_count": 1,
      "settings_account_id": 1,
      "settings_analytics": {},
      "settings_anonymous_responses": true,
      "settings_auto_submission": true,
      "settings_blacklisted_ips": "string",
      "settings_copy_of_response": true,
      "settings_created_at": {},
      "settings_cut_off_date": "string",
      "settings_deleted_at": "string",
      "settings_disable_contact_tracking": true,
      "settings_disable_scroll_back": true,
      "settings_edit_response": true,
      "settings_id": 1,
      "settings_indicator": "string",
      "settings_limit_submission": {},
      "settings_navigation_settings": {},
      "settings_overridden": true,
      "settings_partial_notification": true,
      "settings_partial_submission": true,
      "settings_properties": {},
      "settings_quota_enabled": true,
      "settings_redunant_responses": true,
      "settings_response_limit": 1,
      "settings_self_response": {},
      "settings_send_responses_mail": true,
      "settings_send_thank_you_email": true,
      "settings_short_url_path": "https://example.com",
      "settings_survey_close_page": {},
      "settings_survey_id": 1,
      "settings_thank_you_email": {},
      "settings_throttling": {},
      "settings_track_ip": true,
      "settings_track_location": true,
      "settings_updated_at": {},
      "settings_url_path": "https://example.com",
      "survey_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `created_at` | object |  |
| `id` | number |  |
| `name` | string |  |
| `response_count` | number |  |
| `settings_account_id` | number |  |
| `settings_analytics` | object |  |
| `settings_anonymous_responses` | boolean |  |
| `settings_auto_submission` | boolean |  |
| `settings_blacklisted_ips` | string |  |
| `settings_copy_of_response` | boolean |  |
| `settings_created_at` | object |  |
| `settings_cut_off_date` | string |  |
| `settings_deleted_at` | string |  |
| `settings_disable_contact_tracking` | boolean |  |
| `settings_disable_scroll_back` | boolean |  |
| `settings_edit_response` | boolean |  |
| `settings_id` | number |  |
| `settings_indicator` | string |  |
| `settings_limit_submission` | object |  |
| `settings_navigation_settings` | object |  |
| `settings_overridden` | boolean |  |
| `settings_partial_notification` | boolean |  |
| `settings_partial_submission` | boolean |  |
| `settings_properties` | object |  |
| `settings_quota_enabled` | boolean |  |
| `settings_redunant_responses` | boolean |  |
| `settings_response_limit` | number |  |
| `settings_self_response` | object |  |
| `settings_send_responses_mail` | boolean |  |
| `settings_send_thank_you_email` | boolean |  |
| `settings_short_url_path` | string |  |
| `settings_survey_close_page` | object |  |
| `settings_survey_id` | number |  |
| `settings_thank_you_email` | object |  |
| `settings_throttling` | object |  |
| `settings_track_ip` | boolean |  |
| `settings_track_location` | boolean |  |
| `settings_updated_at` | object |  |
| `settings_url_path` | string |  |
| `survey_type` | string |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `GET /surveys/{{id}}` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey.md) for the provider-specific parameters and requirements.

