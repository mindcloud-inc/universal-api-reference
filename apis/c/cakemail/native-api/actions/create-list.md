# Create List with Cakemail

Creates a new list in Cakemail.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists`
- **Base URL:** `https://api.cakemail.dev`
- **Official documentation:** [Create List](https://cakemail.dev/en/api/list#create-a-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for the Cakemail list. |
| `default_sender.id` | body | `string<string>` | yes | Cakemail sender ID to use as the list default sender. |
| `language` | body | `string` | no | List language locale, such as en_US. |
