# List Alternate Episodes With Episodes with TVMaze Schedule

Retrieves alternate episodes with episode details from TVMaze.

## Endpoint

- **Method:** `GET`
- **Path:** `/alternatelists/{{id}}/alternateepisodes`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Alternate Episodes With Episodes](https://www.tvmaze.com/api#show-alternate-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | TVMaze alternate list ID. |
