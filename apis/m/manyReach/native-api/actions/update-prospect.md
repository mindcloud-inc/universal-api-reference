# Update Prospect with ManyReach

Updates an existing prospect in ManyReach.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.manyreach.com/api/v2/prospects/:id`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Update Prospect](https://api.manyreach.com/api#v2/tag/prospect)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | body | `string` | no | Updated prospect first name. |
| `id` | path | `string` | no | Prospect ID. |
