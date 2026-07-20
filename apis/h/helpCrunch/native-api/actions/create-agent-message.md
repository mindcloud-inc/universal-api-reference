# Create Agent Message with HelpCrunch

Creates an agent message in HelpCrunch.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://api.helpcrunch.com/v1`
- **Official documentation:** [Create Agent Message](https://docs.helpcrunch.com/en/rest-api-v1/create-message-v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agent` | body | `number` | yes |
| `chat` | body | `number` | yes |
| `text` | body | `string` | yes |
| `type` | body | `string` | yes |
