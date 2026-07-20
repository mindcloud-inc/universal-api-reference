# Get Membership with Google Chat

Retrieves details about a Google Chat membership.

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces/:space/members/:member`
- **Base URL:** `https://chat.googleapis.com/v1`
- **Official documentation:** [Get Membership](https://developers.google.com/workspace/chat/api/reference/rest/v1/spaces.members/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space` | path | `string` | yes | Enter only the space ID. If a membership name is spaces/4Oe1TyAAAAE/members/1234567890, enter 4Oe1TyAAAAE here. |
| `member` | path | `string` | yes | Enter the member identifier from the membership resource, or the user's email address when supported. If the membership name is spaces/4Oe1TyAAAAE/members/1234567890, enter 1234567890 here. |
