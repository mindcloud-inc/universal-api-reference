# Update Recipient with MailoPost

Updates an existing recipient in a MailoPost list.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/email/lists/:list_id/recipients/:id`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Update Recipient](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | MailoPost recipient list identifier. |
| `id` | path | `string` | yes | MailoPost recipient identifier. |
| `email` | body | `string` | yes | Recipient email address. |
| `run_triggers` | body | `boolean` | no | Run recipient triggers after the update. |
| `values[]` | body | `array<object>` | no | Recipient parameter values. |
| `tags[]` | body | `array<string>` | no | Recipient tags. |
