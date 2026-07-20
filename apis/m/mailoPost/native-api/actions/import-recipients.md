# Import Recipients with MailoPost

Imports recipients into a MailoPost list.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/lists/:id/recipients/imports`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Import Recipients](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | MailoPost recipient list identifier. |
| `recipients[]` | body | `array<object>` | yes | Recipients to import. |
| `run_triggers` | body | `string` | no | Run triggers during import. |
| `tags[]` | body | `array<string>` | no | Tags applied to imported recipients. |
| `callback_url` | body | `string` | no | Callback URL called when import completes. |
