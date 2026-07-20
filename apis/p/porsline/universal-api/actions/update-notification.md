# Porsline: Update Notification



```
PUT https://connect.mindcloud.co/v1/universal/porsline/latest/actions/update-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porsline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/update-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": 1,
  "notificationId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/porsline/latest/actions/update-notification', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": 1,
    "notificationId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | number | yes | The id of the target survey. |
| `notificationId` | number | yes | Notification ID. |
| `enabled` | boolean | no | Whether the notification is enabled. |
| `sendingMethod` | number | no | Notification sending method. 1: email, 2: sms, 3: webhook. |
| `recipientType` | number | no | Notification recipient type. 1: self notification, 2: question recipient, 3: variable recipient, 4: respondent user, 5: webhook endpoint. |
| `body` | string | no | Notification body. |
| `subject` | string | no | Notification subject. |
| `recipients` | list<string> | no | List of recipient email addresses. |
| `filter` | number | no | Notification filter ID. |
| `questionRecipient` | number | no | Question ID used as recipient source. |
| `variableRecipient` | number | no | Variable ID used as recipient source. |
| `webhookEndpoint` | string | no | Webhook endpoint URL for webhook notifications. |
| `webhookHeaders` | string | no | Webhook headers object for webhook notifications. Default: `{}`. |

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

Through the native Porsline API, this operation is `PATCH /api/v2/surveys/:survey_id/notifications/:pk/` (base URL `https://survey.porsline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-notification.md) for the provider-specific parameters and requirements.

