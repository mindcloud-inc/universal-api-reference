# Update member with WorkAdventure

Updates a member in a WorkAdventure world.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/worlds/:worldSlug/members/:memberIdentifier`
- **Base URL:** `https://admin.workadventu.re`
- **Official documentation:** [Update member](https://docs.workadventu.re/developer/inbound-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `worldSlug` | path | `string` | yes | The world slug from the WorkAdventure world URL. |
| `memberIdentifier` | path | `string` | yes | Member UUID or email address. |
| `name` | body | `string` | no | Name of the Woka. |
| `firstName` | body | `string` | no | First name displayed on the business card. |
| `lastName` | body | `string` | no | Last name displayed on the business card. |
| `phone` | body | `string` | no | Phone number displayed on the business card. |
| `function` | body | `string` | no | Position displayed on the business card. |
| `information` | body | `string` | no | Additional information displayed on the business card. |
| `trivia` | body | `string` | no | Mood or status displayed on the business card. |
| `address` | body | `string` | no | Address displayed on the business card. |
| `token` | body | `string` | no | Optional explicit member token. |
| `tags[]` | body | `array<string>` | no | List of tags associated with the member. |
