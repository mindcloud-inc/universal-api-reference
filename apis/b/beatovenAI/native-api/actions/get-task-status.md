# Get Task Status with Beatoven AI

Retrieves composition task status from Beatoven AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:taskId`
- **Base URL:** `https://public-api.beatoven.ai/api/v1`
- **Official documentation:** [Get Task Status](https://github.com/Beatoven/public-api/blob/main/docs/api-spec.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Beatoven composition task ID returned by a compose request. |
