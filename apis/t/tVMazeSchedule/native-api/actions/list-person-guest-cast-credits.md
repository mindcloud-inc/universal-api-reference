# List Person Guest Cast Credits with TVMaze Schedule

Retrieves guest cast credits for a TVMaze person.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/{{id}}/guestcastcredits`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Person Guest Cast Credits](https://www.tvmaze.com/api#person-guest-cast-credits)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze person ID. |
| `embed` | query | `string` | no | Optional embedded resource name, such as episode or character. |
