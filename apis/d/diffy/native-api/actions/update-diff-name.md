# Update Diff Name with Diffy

Updates a diff name in Diffy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/diffs/:id`
- **Base URL:** `https://app.diffy.website/api`
- **Official documentation:** [Update Diff Name](https://app.diffy.website/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Diff ID. |
| `name` | body | `string` | no | Updated diff name. |
