# Update Sequence with ManyReach

Updates an existing sequence in ManyReach.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.manyreach.com/api/v2/sequences/:id`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Update Sequence](https://api.manyreach.com/api#v2/tag/sequence)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Sequence ID. |
| `name` | body | `string` | no | Updated sequence name. |
