# Delete Repository with Cloudsmith

## Endpoint

- **Method:** `DELETE`
- **Path:** `/repos/:owner/:identifier/`
- **Base URL:** `https://api.cloudsmith.io`
- **Official documentation:** [Delete Repository](https://help.cloudsmith.io/reference/repos_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner namespace slug. |
| `identifier` | path | `string` | yes | Repository identifier or slug. |
