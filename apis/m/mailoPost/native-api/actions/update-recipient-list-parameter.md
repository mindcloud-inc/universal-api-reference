# Update Recipient List Parameter with MailoPost

Updates an existing recipient list parameter in MailoPost.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/email/lists/:list-id/parameters/:id`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Update Recipient List Parameter](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list-id` | path | `string` | yes | MailoPost recipient list identifier. |
| `id` | path | `string` | yes | MailoPost recipient list parameter identifier. |
| `title` | body | `string` | no | Recipient list parameter title. |
| `kind` | body | `string` | no | Recipient list parameter kind. |
