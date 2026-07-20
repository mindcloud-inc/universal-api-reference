# Delete Multiple Messages with DONNAJAMES Easy

Deletes multiple messages from DONNAJAMES Easy.

## Endpoint

- **Method:** `POST`
- **Path:** `messages/delete`
- **Base URL:** `https://app.gpt-trainer.com/api/v1`
- **Official documentation:** [Delete Multiple Messages](https://guide.gpt-trainer.com/api-reference/messages/delete_multi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuids[]` | body | `array<string>` | yes | Message uuids |
