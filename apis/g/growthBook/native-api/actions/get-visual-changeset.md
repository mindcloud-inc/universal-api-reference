# Get a single visual changeset with GrowthBook

Retrieves a visual changeset from your GrowthBook organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/visual-changesets/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get a single visual changeset](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `includeExperiment` | query | `number` | no | Include the associated experiment in payload |
