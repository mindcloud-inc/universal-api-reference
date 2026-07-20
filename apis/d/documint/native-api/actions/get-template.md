# Get Template with Documint

Retrieves a template from Documint by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates/:id`
- **Base URL:** `https://api.documint.me/1`
- **Official documentation:** [Get Template](https://documenter.getpostman.com/view/11741160/TVK5cLxQ)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Documint template ID. |
| `select` | query | `string` | no | Comma-separated list of fields to include in the returned template. |
