# Get Random Joke with Humor API

## Endpoint

- **Method:** `GET`
- **Path:** `/jokes/random`
- **Base URL:** `https://api.humorapi.com`
- **Official documentation:** [Get Random Joke](https://humorapi.com/docs/#Random-Joke)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include-tags` | query | `string` | no | Comma-separated tags the joke should include. |
| `exclude-tags` | query | `string` | no | Comma-separated tags the joke must not include. |
| `min-rating` | query | `number` | no | Minimum rating between 0 and 10. |
| `max-length` | query | `number` | no | Maximum joke length in letters. |
