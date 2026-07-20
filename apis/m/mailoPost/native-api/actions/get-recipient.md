# Get Recipient with MailoPost

Retrieves a recipient from a MailoPost list.

## Endpoint

- **Method:** `GET`
- **Path:** `/email/lists/:list_id/recipients/:id`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Get Recipient](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | MailoPost recipient list identifier. |
| `id` | path | `string` | yes | MailoPost recipient identifier. |
