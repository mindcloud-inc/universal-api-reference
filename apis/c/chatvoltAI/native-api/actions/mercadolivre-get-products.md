# Get Mercado Livre Products with Chatvolt AI

Retrieves Mercado Livre products from Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/mercadolivre/get-products`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Get Mercado Livre Products](https://docs.chatvolt.ai/api-reference/endpoint/mercadolivre/get-products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | query | `string` | yes | The ID of the agent. |
| `query` | query | `string` | no | The search query for fuzzy search. |
| `threshold` | query | `number` | no | The threshold for fuzzy search. |
| `maxResults` | query | `number` | no | The maximum number of results to return. |
| `caseSensitive` | query | `boolean` | no | Whether the search should be case-sensitive. |
| `sortByRelevance` | query | `boolean` | no | Whether to sort the results by relevance. |
| `partialMatch` | query | `boolean` | no | Whether to allow partial matches. |
| `typoTolerance` | query | `number` | no | The typo tolerance for fuzzy search. |
