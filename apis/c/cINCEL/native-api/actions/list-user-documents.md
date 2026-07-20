# List User Documents with CINCEL

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:user/documents`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [List User Documents](https://docs.cincel.digital/v3/digital-signature#get-/users/-user-/documents)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | path | `number` | yes | User ID from the path. |
| `q` | query | `string` | no | Full-text search query. |
| `name_like` | query | `string` | no | Filter documents by name substring. |
| `status[]` | query | `array<string>` | no | Filter documents by status. |
| `feed` | query | `string` | no | Filter documents by feed bucket. |
| `invite_type[]` | query | `array<string>` | no | Filter documents by invite type. |
| `include_deleted` | query | `boolean` | no | Include deleted documents. |
| `created_at_gte` | query | `date` | no | Only include documents created on or after this timestamp. |
| `created_at_lte` | query | `date` | no | Only include documents created on or before this timestamp. |
