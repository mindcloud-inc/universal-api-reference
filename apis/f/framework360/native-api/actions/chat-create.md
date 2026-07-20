# Create Chat with Framework360

## Endpoint

- **Method:** `POST`
- **Path:** `chat/create`
- **Base URL:** `https://mindcloudstage0.framework360.site/m/api`
- **Official documentation:** [Create Chat](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `number` | yes | Customer ID to associate with the conversation. |
| `message` | body | `string` | yes | Initial conversation message. |
| `attachments[]` | body | `array<string>` | no | Optional attachments to include. |
| `type` | body | `string` | no | Conversation type. |
| `subject` | body | `string` | no | Conversation subject. |
