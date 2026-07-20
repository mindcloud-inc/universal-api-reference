# Create Notification with Porsline

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/surveys/:survey_id/notifications/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [Create Notification](https://developers.porsline.com/#tag/Notifications/paths/~1api~1v2~1surveys~1{survey_id}~1notifications~1/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `number` | yes | The id of the target survey. |
| `sending_method` | body | `number` | yes | Notification sending method. 1: email, 2: sms, 3: webhook. |
| `recipient_type` | body | `number` | yes | Notification recipient type. 1: self notification, 2: question recipient, 3: variable recipient, 4: respondent user, 5: webhook endpoint. |
| `body` | body | `string` | yes | Notification body text. |
| `subject` | body | `string` | yes | Email subject. |
| `enabled` | body | `boolean` | no | Whether the notification is enabled. |
| `recipients` | body | `list<string>` | no | List of recipient email addresses. |
| `webhook_endpoint` | body | `string` | no | Webhook endpoint URL for webhook notifications. |
| `filter` | body | `number` | no | Notification filter ID to apply when sending. |
| `question_recipient` | body | `number` | no | Question ID whose answer provides the recipient value. |
| `variable_recipient` | body | `number` | no | Variable ID whose value provides the recipient value. |
| `webhook_headers` | body | `string` | no | Webhook headers object for webhook notifications. |
