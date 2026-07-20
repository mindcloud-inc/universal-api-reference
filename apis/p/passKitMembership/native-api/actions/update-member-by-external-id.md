# Update Member By External ID with PassKit Membership

Updates an existing member in PassKit Membership by external ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/members/member`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Update Member By External ID](https://help.passkit.com/en/articles/4134575-editing-members-through-the-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | body | `string` | yes | Member external id. |
| `person.displayName` | body | `string` | no | Updated display name. |
| `points` | body | `number` | no | Updated points balance. |
| `programId` | body | `string` | yes | PassKit membership program id. |
| `tierId` | body | `string` | no | Updated member tier id. |
