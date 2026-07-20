# Update Business Profile Photo with Gupshup

Updates the business profile photo in Gupshup.

## Endpoint

- **Method:** `PUT`
- **Path:** `/wa/app/{appId}/business/profile/photo`
- **Base URL:** `https://api.gupshup.io`
- **Official documentation:** [Update Business Profile Photo](https://docs.gupshup.io/reference/set-profile-photo)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Gupshup app ID. |
| `photo` | body | `file` | yes | Business profile photo file or media value accepted by Gupshup. |
