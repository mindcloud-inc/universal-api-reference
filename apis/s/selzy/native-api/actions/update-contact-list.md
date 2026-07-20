# Update Contact List with Selzy

Updates an existing contact list in Selzy.

## Endpoint

- **Method:** `POST`
- **Path:** `updateList`
- **Base URL:** `https://api.selzy.com/en/api`
- **Official documentation:** [Update Contact List](https://selzy.com/en/support/api/contacts/updatelist/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | query | `number` | yes | List code from getLists or createList. |
| `title` | query | `string` | yes | Unique contact list name. |
| `before_subscribe_url` | query | `string` | no | Redirect URL shown before confirmed subscription. |
| `after_subscribe_url` | query | `string` | no | Redirect URL shown after successful subscription. |
