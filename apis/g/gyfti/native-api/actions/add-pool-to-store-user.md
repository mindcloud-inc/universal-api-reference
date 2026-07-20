# Add Pool to Store User with gyfti

Adds a pool to a gyfti Store user.

## Endpoint

- **Method:** `POST`
- **Path:** `/wf/add-pool`
- **Base URL:** `https://app.gyfti.fr/api/1.1`
- **Official documentation:** [Add Pool to Store User](https://developer.gyfti.fr/using-gyfti-store/add-a-new-pool-to-your-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_email` | body | `string` | yes | Store user's email address. |
| `user_add_pool` | body | `number` | yes | Amount to add to the store user's pool. |
