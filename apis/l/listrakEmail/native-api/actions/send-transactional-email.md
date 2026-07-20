# Send Transactional Email with Listrak Email

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/List/:listId/TransactionalMessage/:transactionalMessageId/Message`
- **Base URL:** `https://api.listrak.com/email`
- **Official documentation:** [Send Transactional Email](https://api.listrak.com/email#operation/TransactionalMessage_PostTransactionalMessageSend)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `number` | yes | Identifier used to locate the Listrak list. |
| `transactionalMessageId` | path | `number` | yes | Identifier used to locate the previously-created transactional message/template. |
| `emailAddress` | body | `string` | yes | Email address of the contact to send to. |
| `segmentationFieldValues[]` | body | `array<object>` | yes | Array of profile field values used to populate dynamic placeholders in the transactional email template. Each item should include `segmentationFieldId` and `value`. |
| `segmentationFieldValues[].segmentationFieldId` | body | `number` | yes | Numeric API ID of the Listrak profile field used as a template placeholder. |
| `segmentationFieldValues[].value` | body | `string` | yes | Value to populate for this profile field in the transactional email template. |
