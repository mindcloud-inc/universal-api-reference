# Update a Visitor with Linkbreakers

Updates an existing visitor in Linkbreakers.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/visitors/:id`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [Update a Visitor](https://linkbreakers.com/help/api/visitors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the visitor to update. |
| `visitor` | body | `object` | no | Visitor update payload. |
