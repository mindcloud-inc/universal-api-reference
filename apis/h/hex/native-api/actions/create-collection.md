# Create Collection with Hex

## Endpoint

- **Method:** `POST`
- **Path:** `/collections`
- **Base URL:** `https://app.hex.tech/api/v1`
- **Official documentation:** [Create Collection](https://learn.hex.tech/docs/api-integrations/api/reference#operation/CreateCollection)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | no |
| `name` | body | `string` | yes |
| `sharing.groups[].access` | body | `string<string>` | no |
| `sharing.groups[].id` | body | `string<string>` | no |
| `sharing.users[].access` | body | `string<string>` | no |
| `sharing.users[].id` | body | `string<string>` | no |
| `sharing.workspace.members` | body | `string` | no |
