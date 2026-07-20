# Get Person with TVMaze Schedule

Retrieves a person from TVMaze by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/{{id}}`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [Get Person](https://www.tvmaze.com/api#person-main-information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze person ID. |
| `embed` | query | `string` | no | Optional embedded resource name, such as castcredits. |
