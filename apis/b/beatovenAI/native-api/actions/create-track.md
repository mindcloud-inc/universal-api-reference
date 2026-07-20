# Create Track with Beatoven AI

Creates a new track in Beatoven AI from a text prompt.

## Endpoint

- **Method:** `POST`
- **Path:** `/tracks`
- **Base URL:** `https://public-api.beatoven.ai/api/v1`
- **Official documentation:** [Create Track](https://raw.githubusercontent.com/Beatoven/public-api/main/docs/api-spec-old.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt.text` | body | `string` | yes | Text prompt describing the track you want Beatoven to initialize. |
