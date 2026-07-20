# Delete Multiple Sources with DONNAJAMES Easy

Deletes multiple sources from DONNAJAMES Easy.

## Endpoint

- **Method:** `POST`
- **Path:** `data-sources/delete`
- **Base URL:** `https://app.gpt-trainer.com/api/v1`
- **Official documentation:** [Delete Multiple Sources](https://guide.gpt-trainer.com/api-reference/data-sources/delete_multi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuids[]` | body | `array<string>` | yes | Source uuids |
