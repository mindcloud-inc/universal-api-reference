# Compose Track with Beatoven AI

Starts track composition in Beatoven AI from a text prompt.

## Endpoint

- **Method:** `POST`
- **Path:** `/tracks/compose`
- **Base URL:** `https://public-api.beatoven.ai/api/v1`
- **Official documentation:** [Compose Track](https://github.com/Beatoven/public-api/blob/main/docs/api-spec.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt.text` | body | `string` | yes | Text prompt describing the track you want Beatoven to compose. |
| `format` | body | `string` | no | Audio format for the generated track. Supported values are mp3, aac, and wav. Accepted values: `0`, `1`, `2`. |
| `looping` | body | `boolean` | no | Set to true to increase looping in the generated track. |
