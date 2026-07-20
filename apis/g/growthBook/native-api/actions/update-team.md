# Update a single team with GrowthBook

Updates an existing team in GrowthBook.

## Endpoint

- **Method:** `PUT`
- **Path:** `/teams/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update a single team](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `name` | body | `string` | no | — |
| `createdBy` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `role` | body | `string` | no | The global role for members of this team |
| `limitAccessByEnvironment` | body | `boolean` | no | — |
| `environments` | body | `list<string>` | no | An empty array means 'all environments' |
| `projectRoles[]` | body | `array<object>` | no | — |
| `managedBy` | body | `object` | no | — |
| `defaultProject` | body | `string` | no | — |
