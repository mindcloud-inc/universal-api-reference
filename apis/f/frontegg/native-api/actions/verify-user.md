# Verify User with Frontegg

Marks a user as verified in Frontegg.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/resources/users/v1/:userId/verify`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Verify User](https://developers.frontegg.com/ciam/api/identity/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID to verify. |
