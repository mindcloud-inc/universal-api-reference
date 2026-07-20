# List Voices with Uberduck

Retrieves available voice options from Uberduck.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/voices`
- **Base URL:** `https://api.uberduck.ai`
- **Official documentation:** [List Voices](https://docs.uberduck.ai/api-reference/get-voices-v-1-voices-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `age` | query | `string` | no | Filter voices by age. |
| `gender` | query | `string` | no | Filter voices by gender. |
| `accent` | query | `string` | no | Filter voices by accent. |
| `mood` | query | `string` | no | Filter voices by mood. |
| `style` | query | `string` | no | Filter voices by style. |
| `language` | query | `string` | no | Filter voices by language. |
| `limit` | query | `number` | no | Maximum number of voices to return. |
| `offset` | query | `number` | no | Number of voices to skip. |
| `private` | query | `boolean` | no | Whether to include private voices. |
| `name` | query | `string` | no | Filter voices by name. |
| `uuid` | query | `string` | no | Filter voices by voice UUID. |
| `model` | query | `string` | no | Filter voices by model ID. |
| `tag` | query | `string` | no | Filter voices by tag. |
| `search_term` | query | `string` | no | Keyword search across voice name and display name. |
