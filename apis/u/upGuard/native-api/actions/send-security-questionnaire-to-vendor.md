# Send Security Questionnaire To Vendor with UpGuard

Sends a security questionnaire to a vendor in UpGuard.

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/questionnaire`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [Send Security Questionnaire To Vendor](https://cyber-risk.upguard.com/api/docs#operation/sendQuestionnaire)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_message` | body | `string` | no | Optional questionnaire email message. |
| `email_title` | body | `string` | no | Optional questionnaire email title. |
| `questionnaire_type_id` | body | `number` | yes | The numeric ID of the questionnaire type to send. |
| `reminder_date` | body | `string` | no | Optional future ISO 8601 reminder date. |
| `sender_email` | body | `string` | yes | The email address of the questionnaire sender. |
| `due_date` | body | `string` | yes | The future ISO 8601 due date for the questionnaire. |
| `recipients[]` | body | `array<object>` | yes | The list of questionnaire recipients. |
| `risk_information_visiblity` | body | `string` | yes | The visibility level of risk information in the questionnaire. |
| `vendor_primary_hostname` | body | `string` | no | The primary hostname of the vendor to which the questionnaire will be sent. |
| `vendor_id` | body | `number` | no | The vendor ID to which the questionnaire will be sent. |
