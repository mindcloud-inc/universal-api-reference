# List Memberships with Google Chat

Retrieves memberships in a Google Chat space.

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces/:space/members`
- **Base URL:** `https://chat.googleapis.com/v1`
- **Official documentation:** [List Memberships](https://developers.google.com/workspace/chat/api/reference/rest/v1/spaces.members/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space` | path | `string` | yes | Enter only the space ID from the List Spaces result. If the result shows spaces/4Oe1TyAAAAE, enter 4Oe1TyAAAAE here. |
| `filter` | query | `string` | no | Optional. Filter memberships by supported member fields. |
| `showGroups` | query | `boolean` | no | Optional. Include group memberships when true. |
| `showInvited` | query | `boolean` | no | Optional. Include invited memberships when true. |
