# Create a single team with GrowthBook

Creates a new team in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a single team](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `createdBy` | body | `string` | no | — |
| `description` | body | `string` | yes | — |
| `role` | body | `string` | yes | The global role for members of this team |
| `limitAccessByEnvironment` | body | `boolean` | no | — |
| `environments` | body | `list<string>` | no | An empty array means 'all environments' |
| `projectRoles[]` | body | `array<object>` | no | — |
| `managedBy` | body | `object` | no | — |
| `defaultProject` | body | `string` | no | — |
