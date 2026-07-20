# Update a single archetype with GrowthBook

Updates an existing archetype in GrowthBook.

## Endpoint

- **Method:** `PUT`
- **Path:** `/archetypes/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update a single archetype](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `name` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `isPublic` | body | `boolean` | no | Whether to make this Archetype available to other team members |
| `attributes` | body | `object` | no | The attributes to set when using this Archetype |
| `projects` | body | `list<string>` | no | — |
