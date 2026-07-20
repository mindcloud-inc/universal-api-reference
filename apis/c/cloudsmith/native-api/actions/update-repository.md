# Update Repository with Cloudsmith

## Endpoint

- **Method:** `PATCH`
- **Path:** `/repos/:owner/:identifier/`
- **Base URL:** `https://api.cloudsmith.io`
- **Official documentation:** [Update Repository](https://help.cloudsmith.io/reference/repos_partial_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner namespace slug. |
| `identifier` | path | `string` | yes | Repository identifier or slug. |
| `name` | body | `string` | no | Updated repository name. |
| `description` | body | `string` | no | Updated repository description. |
