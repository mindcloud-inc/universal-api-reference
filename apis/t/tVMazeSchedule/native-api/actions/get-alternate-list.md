# Get Alternate List with TVMaze Schedule

Retrieves an alternate list from TVMaze.

## Endpoint

- **Method:** `GET`
- **Path:** `/alternatelists/{{id}}`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [Get Alternate List](https://www.tvmaze.com/api#show-alternate-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze alternate list ID. |
| `embed` | query | `string` | no | Optional embedded resource name, such as alternateepisodes. |
