# Create Joke with Humor API

## Endpoint

- **Method:** `GET`
- **Path:** `/jokes/create`
- **Base URL:** `https://api.humorapi.com`
- **Official documentation:** [Create Joke](https://humorapi.com/docs/#Create-Joke)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topics` | query | `string` | no | Comma-separated topics the generated joke should be about. |
| `max-length` | query | `number` | no | Maximum joke length in letters. |
