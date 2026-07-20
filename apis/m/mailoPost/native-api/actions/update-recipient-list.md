# Update Recipient List with MailoPost

Updates an existing recipient list in MailoPost.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/email/lists/:id`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Update Recipient List](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | MailoPost recipient list identifier. |
| `title` | body | `string` | yes | Recipient list title. |
