# Fetch All Sessions with DONNAJAMES Easy

Retrieves all sessions for a chatbot from DONNAJAMES Easy.

## Endpoint

- **Method:** `GET`
- **Path:** `chatbot/:uuid/sessions`
- **Base URL:** `https://app.gpt-trainer.com/api/v1`
- **Official documentation:** [Fetch All Sessions](https://guide.gpt-trainer.com/api-reference/sessions/fetch_multi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_timestamp` | query | `string` | no | Filter sessions created before this ISO 8601 timestamp. |
| `start_timestamp` | query | `string` | no | Filter sessions created after this ISO 8601 timestamp. |
| `uuid` | path | `string` | yes | Chatbot uuid |
