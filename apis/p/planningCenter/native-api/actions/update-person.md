# Update Person with Planning Center

Updates an existing person in Planning Center.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/people/v2/people/:id`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [Update Person](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `data` | body | `object` | yes | JSON:API resource object containing the Person type, attributes, and optional relationships to update. |
| `include` | query | `string` | no | — |
