# Porsline: Create Notification



```
POST https://connect.mindcloud.co/v1/universal/porsline/latest/actions/create-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porsline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/create-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "survey_id": 1,
  "sending_method": 1,
  "recipient_type": 1,
  "body": "string",
  "subject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/porsline/latest/actions/create-notification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "survey_id": 1,
    "sending_method": 1,
    "recipient_type": 1,
    "body": "string",
    "subject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `survey_id` | number | yes | The id of the target survey. |
| `sending_method` | number | yes | Notification sending method. 1: email, 2: sms, 3: webhook. |
| `recipient_type` | number | yes | Notification recipient type. 1: self notification, 2: question recipient, 3: variable recipient, 4: respondent user, 5: webhook endpoint. |
| `body` | string | yes | Notification body text. |
| `subject` | string | yes | Email subject. |
| `enabled` | boolean | no | Whether the notification is enabled. |
| `recipients` | list<string> | no | List of recipient email addresses. |
| `webhookEndpoint` | string | no | Webhook endpoint URL for webhook notifications. |
| `filter` | number | no | Notification filter ID to apply when sending. |
| `questionRecipient` | number | no | Question ID whose answer provides the recipient value. |
| `variableRecipient` | number | no | Variable ID whose value provides the recipient value. |
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
      "recipientType": 1,
      "sendingMethod": 1,
      "survey": 1,
      "template": "string",
      "webhookEndpoint": "string",
      "webhookMethod": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string | Notification body. |
| `enabled` | boolean | Whether the notification is enabled. |
| `filter` | number | Filter ID when present. |
| `id` | number | Notification ID. |
| `recipientType` | number | Porsline recipient type. |
| `sendingMethod` | number | Porsline sending method. |
| `survey` | number | Owning survey ID. |
| `template` | string | Notification template when present. |
| `webhookEndpoint` | string | Webhook endpoint when using webhook notifications. |
| `webhookMethod` | string | Webhook HTTP method when using webhook notifications. |

## Native endpoint

Through the native Porsline API, this operation is `POST /api/v2/surveys/:survey_id/notifications/` (base URL `https://survey.porsline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-notification.md) for the provider-specific parameters and requirements.

