# Reply Chat with Framework360

## Endpoint

- **Method:** `POST`
- **Path:** `chat/reply`
- **Base URL:** `https://mindcloudstage0.framework360.site/m/api`
- **Official documentation:** [Reply Chat](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation` | body | `number` | yes | Conversation ID to reply to. |
| `message` | body | `string` | yes | Reply message text. |
| `attachments[]` | body | `array<string>` | no | Optional reply attachments. |
