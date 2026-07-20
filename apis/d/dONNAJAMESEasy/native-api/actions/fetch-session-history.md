# Fetch Session History with DONNAJAMES Easy

Retrieves a session transcript from DONNAJAMES Easy.

## Endpoint

- **Method:** `GET`
- **Path:** `session/:uuid/messages/plain-text`
- **Base URL:** `https://app.gpt-trainer.com/api/v1`
- **Official documentation:** [Fetch Session History](https://guide.gpt-trainer.com/api-reference/messages/fetch-message-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Session uuid |
