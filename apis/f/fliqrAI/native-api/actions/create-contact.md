# Create Contact with Fliqr AI

Creates a new contact in Fliqr AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://app.fliqr.ai/api/`
- **Official documentation:** [Create Contact](https://docs.fliqr.ai/api-reference/users/post-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | body | `string` | yes | Phone number with country code. |
| `first_name` | body | `string` | no | Contact first name. |
| `last_name` | body | `string` | no | Contact last name. |
| `gender` | body | `string` | no | Contact gender. Accepted values: `0`, `1`, `2`. |
| `actions[]` | body | `array<object>` | no | Actions to perform when creating the contact. |
