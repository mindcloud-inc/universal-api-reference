# Add or Update Store User with gyfti

Adds or updates a user in gyfti Store.

## Endpoint

- **Method:** `POST`
- **Path:** `/wf/add-user-store`
- **Base URL:** `https://app.gyfti.fr/api/1.1`
- **Official documentation:** [Add or Update Store User](https://developer.gyfti.fr/using-gyfti-store/add-or-update-a-user-in-your-store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_firstname` | body | `string` | yes | Store user's first name. |
| `user_lastname` | body | `string` | yes | Store user's last name. |
| `user_email` | body | `string` | yes | Store user's email address. |
| `user_pool` | body | `number` | no | Optional initial pool amount when creating the store user. |
