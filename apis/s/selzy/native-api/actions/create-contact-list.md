# Create Contact List with Selzy

Creates a new contact list in Selzy.

## Endpoint

- **Method:** `POST`
- **Path:** `createList`
- **Base URL:** `https://api.selzy.com/en/api`
- **Official documentation:** [Create Contact List](https://selzy.com/en/support/api/contacts/createlist/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | query | `string` | yes | Unique contact list name. |
| `before_subscribe_url` | query | `string` | no | Redirect URL shown before confirmed subscription. |
| `after_subscribe_url` | query | `string` | no | Redirect URL shown after successful subscription. |
