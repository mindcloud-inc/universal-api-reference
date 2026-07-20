# Set Member Tier Points By External ID with PassKit Membership

Updates a member's tier points in PassKit Membership by external ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/members/member`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Set Member Tier Points By External ID](https://help.passkit.com/en/articles/4134575-editing-members-through-the-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | body | `string` | yes | Member external id. |
| `programId` | body | `string` | yes | PassKit membership program id. |
| `tierPoints` | body | `number` | yes | Tier points balance to set. |
