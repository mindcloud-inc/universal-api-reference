# Update Resource with Schedule It

Updates an existing resource in Schedule It.

## Endpoint

- **Method:** `POST`
- **Path:** `/resources/:id`
- **Base URL:** `https://www.scheduleit.com/api`
- **Official documentation:** [Update Resource](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The resource ID. |
| `name` | body | `string` | no | The updated resource name. |
| `email` | body | `string` | no | The updated resource email address. |
| `data1` | body | `string` | no | The updated first resource details field. |
