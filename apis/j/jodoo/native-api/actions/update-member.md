# Update Member with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `/corp/user/update`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [Update Member](https://help.jodoo.com/en/articles/9992457-member-update-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | body | `string` | yes | Username of the member to update. Jodoo only allows letters, digits, and underscores. |
| `name` | body | `string` | yes | Updated display name for the member. |
| `departments[]` | body | `array<number>` | yes | Array of department numbers for the member. |
