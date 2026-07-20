# Update Matter with Clio Manage

Updates a matter in Clio Manage by matter ID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/matters/:id.json`
- **Base URL:** `https://app.clio.com/api/v4`
- **Official documentation:** [Update Matter](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Matters/operation/Matter%23update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `data.description` | body | `string` | no | — |
| `data.status` | body | `list` | no | Accepted values: `closed`, `open`, `pending`. |
