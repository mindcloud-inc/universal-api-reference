# Lock User with Frontegg

Updates a user's lock status in Frontegg.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/resources/users/v1/:userId/lock`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Lock User](https://developers.frontegg.com/ciam/api/identity/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The user ID to lock. |
