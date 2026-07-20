# Remove Study User with Castor EDC

Deletes a study user from Castor EDC.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/study/:study_id/user/:user_id`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [Remove Study User](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The Castor study UUID. |
| `user_id` | path | `string` | yes | The study user UUID. |
