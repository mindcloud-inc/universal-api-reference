# Create Member with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `/corp/user/create`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [Create Member](https://help.jodoo.com/en/articles/9992456-member-adding-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | body | `string` | yes | Username for the new member. Jodoo only allows letters, digits, and underscores. |
| `name` | body | `string` | yes | Display name for the new member. |
| `departments[]` | body | `array<number>` | yes | Array of department numbers for the new member. |
