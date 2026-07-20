# Create Questionnaire with Conveyor

Creates a questionnaire record in Conveyor.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/questionnaires`
- **Base URL:** `https://api.conveyor.com/api`
- **Official documentation:** [Create Questionnaire](https://docs.conveyor.com/reference/post-questionnaires)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content_type` | body | `string` | no | Uploaded questionnaire content type. |
| `content_version_id` | body | `string` | no | Salesforce content version identifier. |
| `crm_id` | body | `string` | no | CRM identifier associated with the questionnaire. |
| `customer_name` | body | `string` | no | Customer name associated with the questionnaire. |
| `domain` | body | `string` | yes | Company domain for the questionnaire. |
| `filename` | body | `string` | no | Uploaded questionnaire filename. |
| `notes` | body | `string` | no | Additional questionnaire notes. |
| `portal_url` | body | `string` | no | Portal URL for portal-based questionnaires. |
| `questionnaire_type` | body | `string` | no | Questionnaire type. |
| `email` | body | `string` | yes | Recipient or customer email for the questionnaire. |
| `original_format` | body | `string` | yes | Original questionnaire format. |
| `due_at` | body | `date` | no | Questionnaire due date. |
| `product_line_ids` | body | `string<string>` | no | Product line identifiers to associate with the questionnaire. |
| `file` | body | `file` | no | Questionnaire file upload. |
| `crm_amount` | body | `number` | no | CRM deal amount associated with the questionnaire. |
