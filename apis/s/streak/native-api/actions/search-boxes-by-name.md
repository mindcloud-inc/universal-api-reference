# Search Boxes By Name with Streak

Finds boxes in Streak by exact name.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/search`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [Search Boxes By Name](https://streak.readme.io/reference/searchng-for-boxes-by-name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Exact box name to search for. |
| `pipelineKey` | query | `string<string>` | no | Limit box results to one or more pipelines. Send multiple values as a array. |
| `stageKey` | query | `string<string>` | no | Limit box results to one or more stages. Send multiple values as a array. |
