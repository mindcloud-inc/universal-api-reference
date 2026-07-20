# Update List with Cakemail

Updates an existing list in Cakemail.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/lists/:listId`
- **Base URL:** `https://api.cakemail.dev`
- **Official documentation:** [Update List](https://cakemail.dev/en/api/list#update-a-list-parameters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `number` | yes | Cakemail list ID. |
| `name` | body | `string` | no | Updated list name. |
| `default_sender.id` | body | `string<string>` | no | Cakemail sender ID to use as the list default sender. |
| `language` | body | `string` | no | Updated list language locale, such as en_US. |
