# Update Source with DONNAJAMES Easy

Updates an existing source in DONNAJAMES Easy.

## Endpoint

- **Method:** `POST`
- **Path:** `data-source/:uuid/update`
- **Base URL:** `https://app.gpt-trainer.com/api/v1`
- **Official documentation:** [Update Source](https://guide.gpt-trainer.com/api-reference/data-sources/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Data source uuid |
| `title` | body | `string` | yes | — |
