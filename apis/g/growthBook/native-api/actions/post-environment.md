# Create a new environment with GrowthBook

Creates a new environment in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/environments`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a new environment](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The ID of the new environment |
| `description` | body | `string` | no | The description of the new environment |
| `toggleOnList` | body | `boolean` | no | Show toggle on feature list |
| `defaultState` | body | `boolean` | no | Default state for new features |
| `projects` | body | `list<string>` | no | — |
| `parent` | body | `string` | no | An environment that the new environment should inherit feature rules from. Requires an enterprise license |
