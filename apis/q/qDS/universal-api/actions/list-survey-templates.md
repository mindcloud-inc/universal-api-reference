# QDS: List Survey Templates



```
GET https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-survey-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QDS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-survey-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-survey-templates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "surveytemplates": [
        {
          "alert_fail_emails": "ava@example.com",
          "alert_tip_emails": "ava@example.com",
          "body": "string",
          "id": 1,
          "is_default": true,
          "is_default_employee": true,
          "is_resend_default": true,
          "is_system_template": true,
          "is_tipping_enable": true,
          "name": "Ava Chen",
          "notification_emails": "ava@example.com",
          "post_survey_fail_message": "string",
          "post_survey_fail_url": "https://example.com",
          "post_survey_message": "string",
          "post_survey_url": "https://example.com",
          "question": "string",
          "reply_to": "string",
          "salutation": "string",
          "scaletype_name": "Ava Chen",
          "subject": "string",
          "tipping_heading": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `surveytemplates[].alert_fail_emails` | string |  |
| `surveytemplates[].alert_tip_emails` | string |  |
| `surveytemplates[].body` | string |  |
| `surveytemplates[].id` | number |  |
| `surveytemplates[].is_default` | boolean |  |
| `surveytemplates[].is_default_employee` | boolean |  |
| `surveytemplates[].is_resend_default` | boolean |  |
| `surveytemplates[].is_system_template` | boolean |  |
| `surveytemplates[].is_tipping_enable` | boolean |  |
| `surveytemplates[].name` | string |  |
| `surveytemplates[].notification_emails` | string |  |
| `surveytemplates[].post_survey_fail_message` | string |  |
| `surveytemplates[].post_survey_fail_url` | string |  |
| `surveytemplates[].post_survey_message` | string |  |
| `surveytemplates[].post_survey_url` | string |  |
| `surveytemplates[].question` | string |  |
| `surveytemplates[].reply_to` | string |  |
| `surveytemplates[].salutation` | string |  |
| `surveytemplates[].scaletype_name` | string |  |
| `surveytemplates[].subject` | string |  |
| `surveytemplates[].tipping_heading` | string |  |

## Native endpoint

Through the native QDS API, this operation is `GET /surveytemplates` (base URL `https://qdsapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-survey-templates.md) for the provider-specific parameters and requirements.

