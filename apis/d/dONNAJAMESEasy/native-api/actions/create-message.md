# Create Message with DONNAJAMES Easy

Creates a new session message in DONNAJAMES Easy.

## Endpoint

- **Method:** `POST`
- **Path:** `session/:uuid/message/stream`
- **Base URL:** `https://app.gpt-trainer.com/api/v1`
- **Official documentation:** [Create Message](https://guide.gpt-trainer.com/api-reference/messages/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Session uuid |
| `query` | body | `string` | yes | — |
