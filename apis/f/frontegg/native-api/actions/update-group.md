# Update Group with Frontegg

Updates an existing user group in Frontegg.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/identity/resources/groups/v1/:id`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Update Group](https://developers.frontegg.com/ciam/api/identity/user-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Group ID. |
| `name` | body | `string` | no | Updated group name. |
| `color` | body | `string` | no | Updated group color. |
| `description` | body | `string` | no | Updated group description. |
| `metadata` | body | `string` | no | Updated stringified JSON metadata. |
