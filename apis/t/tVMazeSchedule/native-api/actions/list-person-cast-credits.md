# List Person Cast Credits with TVMaze Schedule

Retrieves cast credits for a TVMaze person.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/{{id}}/castcredits`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Person Cast Credits](https://www.tvmaze.com/api#person-cast-credits)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze person ID. |
| `embed` | query | `string` | no | Optional embedded resource name, such as show or character. |
