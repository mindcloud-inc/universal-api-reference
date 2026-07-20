# Search Summarizer with Perigon

Generates Perigon news summaries from a custom prompt.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/summarize`
- **Base URL:** `https://api.perigon.io/v1`
- **Official documentation:** [Search Summarizer](https://docs.perigon.io/docs/search-summarizer)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | no | — |
| `maxArticleCount` | body | `number` | no | — |
| `returnedArticleCount` | body | `number` | no | — |
| `summarizeFields` | body | `string` | no | Send multiple values as a array. |
| `method` | body | `string` | no | — |
| `model` | body | `string` | no | — |
| `temperature` | body | `number` | no | — |
| `topP` | body | `number` | no | — |
| `maxTokens` | body | `number` | no | — |
| `q` | query | `string` | no | — |
| `sortBy` | query | `string` | no | — |
| `size` | query | `number` | no | — |
| `from` | query | `date` | no | — |
| `to` | query | `date` | no | — |
| `source` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `category` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `topic` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `country` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `companyName` | query | `string` | no | — |
| `showNumResults` | query | `boolean` | no | — |
