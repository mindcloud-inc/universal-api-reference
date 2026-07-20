# Create a visual changeset for an experiment with GrowthBook

Creates a visual changeset for a GrowthBook experiment.

## Endpoint

- **Method:** `POST`
- **Path:** `/experiments/:id/visual-changesets`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a visual changeset for an experiment](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `editorUrl` | body | `string` | yes | URL of the page opened in the visual editor when creating this changeset |
| `urlPatterns[]` | body | `array<object>` | yes | URL patterns that determine which pages this visual changeset applies to |
| `urlPatterns[]` | body | `array<object>` | yes | URL patterns that determine which pages this visual changeset applies to |
