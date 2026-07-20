# Update Collection with Hex

## Endpoint

- **Method:** `PATCH`
- **Path:** `/collections/{collectionId}`
- **Base URL:** `https://app.hex.tech/api/v1`
- **Official documentation:** [Update Collection](https://learn.hex.tech/docs/api-integrations/api/reference#operation/EditCollection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Unique ID for a collection. |
| `description` | body | `string` | no | — |
| `name` | body | `string` | no | — |
| `sharing.upsert.groups[].access` | body | `string<string>` | no | — |
| `sharing.upsert.groups[].id` | body | `string<string>` | no | — |
| `sharing.upsert.users[].access` | body | `string<string>` | no | — |
| `sharing.upsert.users[].id` | body | `string<string>` | no | — |
| `sharing.upsert.workspace.members` | body | `string` | no | — |
