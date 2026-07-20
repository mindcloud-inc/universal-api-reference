# Update Group with Schedule It

Updates an existing group in Schedule It.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:id`
- **Base URL:** `https://www.scheduleit.com/api`
- **Official documentation:** [Update Group](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The group ID. |
| `name` | body | `string` | no | The updated group name. |
| `color_back` | body | `string` | no | The updated group background color. |
