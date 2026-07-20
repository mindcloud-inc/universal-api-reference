# Create Sequence Email with Bento Now

Creates an email template in a Bento Now sequence.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/fetch/sequences/:id/emails/templates`
- **Base URL:** `https://app.bentonow.com/api`
- **Official documentation:** [Create Sequence Email](https://bentonow.com/docs/sequences_api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_template.html` | body | `string` | yes | — |
| `email_template.subject` | body | `string` | yes | — |
| `id` | path | `string` | yes | — |
| `email_template.delay_interval` | body | `string` | no | Optional delay unit: minutes, hours, days, or months. |
| `email_template.delay_interval_count` | body | `number` | no | Optional delay amount used with Delay Interval. |
| `email_template.editor_choice` | body | `string` | no | Optional editor mode. |
| `email_template.inbox_snippet` | body | `string` | no | Optional preview text snippet. |
