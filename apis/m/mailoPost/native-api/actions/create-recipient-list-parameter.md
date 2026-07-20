# Create Recipient List Parameter with MailoPost

Creates a new recipient list parameter in MailoPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/lists/:id/parameters`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Create Recipient List Parameter](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | MailoPost recipient list identifier. |
| `title` | body | `string` | yes | Recipient list parameter title. |
| `kind` | body | `string` | yes | Recipient list parameter kind. |
