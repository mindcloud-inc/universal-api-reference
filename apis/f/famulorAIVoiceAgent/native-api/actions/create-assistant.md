# Create Assistant with Famulor AI - Voice Agent

Creates a new AI assistant in Famulor.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/assistant`
- **Base URL:** `https://app.famulor.de/api`
- **Official documentation:** [Create Assistant](https://docs.famulor.io/en/api-reference/assistants/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | body | `number` | yes | Language ID for the assistant. |
| `name` | body | `string` | yes | Assistant display name. |
| `voice_id` | body | `number` | yes | Voice ID for the assistant. |
