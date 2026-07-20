# Delete User Certificate with Verifalia

Deletes a user certificate from Verifalia.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users/{user-id}/certificates/{certificate-id}`
- **Base URL:** `https://api-1.verifalia.com/v2.7`
- **Official documentation:** [Delete User Certificate](https://verifalia.com/developers/users/client-certificates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user-id` | path | `string` | yes | The Verifalia user ID. |
| `certificate-id` | path | `string` | yes | The Verifalia client certificate ID. |
