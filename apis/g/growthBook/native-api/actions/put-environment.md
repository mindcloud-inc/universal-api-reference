# Update an environment with GrowthBook

Updates an existing environment in GrowthBook.

## Endpoint

- **Method:** `PUT`
- **Path:** `/environments/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update an environment](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `description` | body | `string` | no | The description of the new environment |
| `toggleOnList` | body | `boolean` | no | Show toggle on feature list |
| `defaultState` | body | `boolean` | no | Default state for new features |
| `projects` | body | `list<string>` | no | — |
