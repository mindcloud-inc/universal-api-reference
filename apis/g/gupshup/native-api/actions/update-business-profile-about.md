# Update Business Profile About with Gupshup

Updates the business profile about text in Gupshup.

## Endpoint

- **Method:** `PUT`
- **Path:** `/wa/app/{appId}/business/profile/about`
- **Base URL:** `https://api.gupshup.io`
- **Official documentation:** [Update Business Profile About](https://docs.gupshup.io/reference/set-profile-about)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Gupshup app ID. |
| `about` | body | `string` | yes | Business profile about text. |
