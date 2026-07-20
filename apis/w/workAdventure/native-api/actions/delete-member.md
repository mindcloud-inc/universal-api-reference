# Delete member with WorkAdventure

Deletes a member from a WorkAdventure world.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/worlds/:worldSlug/members/:memberIdentifier`
- **Base URL:** `https://admin.workadventu.re`
- **Official documentation:** [Delete member](https://docs.workadventu.re/developer/inbound-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `worldSlug` | path | `string` | yes | The world slug from the WorkAdventure world URL. |
| `memberIdentifier` | path | `string` | yes | Member UUID or email address. |
