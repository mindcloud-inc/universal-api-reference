# Merge Template with Documint

Creates a document from a template in Documint.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/:id/content`
- **Base URL:** `https://api.documint.me/1`
- **Official documentation:** [Merge Template](https://documenter.getpostman.com/view/11741160/TVK5cLxQ)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Documint template ID to merge. |
| `ignore_fields` | query | `string` | no | Comma-separated template fields to ignore during merge. |
| `watch_fields` | query | `string` | no | Fields to watch during merge preview/debugging. |
