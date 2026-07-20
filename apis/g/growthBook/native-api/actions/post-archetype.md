# Create a single archetype with GrowthBook

Creates a new archetype in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/archetypes`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a single archetype](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `description` | body | `string` | no | — |
| `isPublic` | body | `boolean` | yes | Whether to make this Archetype available to other team members |
| `attributes` | body | `object` | no | The attributes to set when using this Archetype |
| `projects` | body | `list<string>` | no | — |
