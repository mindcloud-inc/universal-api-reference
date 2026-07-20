# Porsline: Get Notification



```
GET https://connect.mindcloud.co/v1/universal/porsline/latest/actions/get-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porsline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/get-notification?connectionId=$CONNECTION_ID&surveyId=213151&notificationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "213151",
  "notificationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/porsline/latest/actions/get-notification?${params}`, {
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
| `surveyId` | number | yes | The id of the target survey. Example: `213151`. |
| `notificationId` | number | yes | Notification ID. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "enabled": true,
      "filter": 1,
      "id": 1,
      "question_recipient": 1,
      "recipient_type": 1,
      "recipients": [
        "string"
      ],
      "sending_method": 1,
      "subject": "string",
      "survey": 1,
      "template": {},
      "variable_recipient": 1,
      "webhook_endpoint": "string",
      "webhook_headers": {},
      "webhook_method": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `enabled` | boolean |  |
| `filter` | number |  |
| `id` | number |  |
| `question_recipient` | number |  |
| `recipient_type` | number |  |
| `recipients` | array<string> |  |
| `sending_method` | number |  |
| `subject` | string |  |
| `survey` | number |  |
| `template` | object |  |
| `variable_recipient` | number |  |
| `webhook_endpoint` | string |  |
| `webhook_headers` | object |  |
| `webhook_method` | string |  |

## Native endpoint

Through the native Porsline API, this operation is `GET /api/v2/surveys/:survey_id/notifications/:pk/` (base URL `https://survey.porsline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notification.md) for the provider-specific parameters and requirements.

