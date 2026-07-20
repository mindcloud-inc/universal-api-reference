# Update Member with PassKit Membership

Updates an existing member in PassKit Membership.

## Endpoint

- **Method:** `PUT`
- **Path:** `/members/member`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Update Member](https://help.passkit.com/en/articles/4134575-editing-members-through-the-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | PassKit member id to update. |
| `person.displayName` | body | `string` | no | Updated member display name. |
| `points` | body | `number` | no | Updated points balance for the member. |
| `tierId` | body | `string` | no | Updated tier id for the member. |
