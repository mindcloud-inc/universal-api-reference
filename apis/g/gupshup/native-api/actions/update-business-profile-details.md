# Update Business Profile Details with Gupshup

Updates business profile details in Gupshup.

## Endpoint

- **Method:** `PUT`
- **Path:** `/wa/app/{appId}/business/profile`
- **Base URL:** `https://api.gupshup.io`
- **Official documentation:** [Update Business Profile Details](https://docs.gupshup.io/reference/set-profile-details)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Gupshup app ID. |
| `description` | body | `string` | no | Business profile description. |
| `email` | body | `string` | no | Business email address. |
| `address` | body | `object` | no | Business address details. |
| `websites[]` | body | `array<string>` | no | Business website URLs. |
