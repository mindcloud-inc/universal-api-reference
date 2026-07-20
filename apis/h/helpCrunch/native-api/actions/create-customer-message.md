# Create Customer Message with HelpCrunch

Creates a customer message in HelpCrunch.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://api.helpcrunch.com/v1`
- **Official documentation:** [Create Customer Message](https://docs.helpcrunch.com/en/rest-api-v1/create-message-v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chat` | body | `number` | yes |
| `text` | body | `string` | yes |
| `type` | body | `string` | yes |
