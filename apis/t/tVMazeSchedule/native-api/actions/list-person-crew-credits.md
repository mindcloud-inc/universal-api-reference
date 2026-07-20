# List Person Crew Credits with TVMaze Schedule

Retrieves crew credits for a TVMaze person.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/{{id}}/crewcredits`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Person Crew Credits](https://www.tvmaze.com/api#person-crew-credits)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze person ID. |
| `embed` | query | `string` | no | Optional embedded resource name, such as show. |
