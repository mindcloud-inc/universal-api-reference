# Unlock User with Frontegg

Unlocks a locked user in Frontegg.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/resources/users/v1/:userId/unlock`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Unlock User](https://developers.frontegg.com/ciam/api/identity/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The user ID to unlock. |
