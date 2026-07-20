# List Alternate Episodes with TVMaze Schedule

Retrieves alternate episodes for a TVMaze list.

## Endpoint

- **Method:** `GET`
- **Path:** `/alternatelists/{{id}}/alternateepisodes`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Alternate Episodes](https://www.tvmaze.com/api#show-alternate-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze alternate list ID. |
| `embed` | query | `string` | no | Optional embedded resource name, such as episodes. |
