# List Dubbing Projects with Murf Dub

Retrieves dubbing projects from Murf Dub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/murfdub/projects/list`
- **Base URL:** `https://api.murf.ai`
- **Official documentation:** [List Dubbing Projects](https://murf.ai/api/docs/api-reference/dubbing/projects/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of projects to return. |
| `next` | query | `string` | no | Next page iterator returned by the previous response. |
