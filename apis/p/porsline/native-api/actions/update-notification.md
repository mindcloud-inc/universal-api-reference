# Update Notification with Porsline

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/surveys/:survey_id/notifications/:pk/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [Update Notification](https://developers.porsline.com/#tag/Notifications/paths/~1api~1v2~1surveys~1{survey_id}~1notifications~1{pk}~1/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `number` | yes | The id of the target survey. |
| `pk` | path | `number` | yes | Notification ID. |
| `enabled` | body | `boolean` | no | Whether the notification is enabled. |
| `sending_method` | body | `number` | no | Notification sending method. 1: email, 2: sms, 3: webhook. |
| `recipient_type` | body | `number` | no | Notification recipient type. 1: self notification, 2: question recipient, 3: variable recipient, 4: respondent user, 5: webhook endpoint. |
| `body` | body | `string` | no | Notification body. |
| `subject` | body | `string` | no | Notification subject. |
| `recipients` | body | `list<string>` | no | List of recipient email addresses. |
| `filter` | body | `number` | no | Notification filter ID. |
| `question_recipient` | body | `number` | no | Question ID used as recipient source. |
| `variable_recipient` | body | `number` | no | Variable ID used as recipient source. |
| `webhook_endpoint` | body | `string` | no | Webhook endpoint URL for webhook notifications. |
| `webhook_headers` | body | `string` | no | Webhook headers object for webhook notifications. |
