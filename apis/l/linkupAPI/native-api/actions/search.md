# Search with LinkupAPI

Finds web content in LinkupAPI by query.

## Endpoint

- **Method:** `POST`
- **Path:** `/search`
- **Base URL:** `https://api.linkup.so/v1`
- **Official documentation:** [Search](https://docs.linkup.so/pages/documentation/api-reference/endpoint/post-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | body | `string` | yes | The natural-language question to search for. |
| `depth` | body | `string` | yes | How deeply Linkup should search for results. Accepted values: `0`, `1`, `2`. |
| `outputType` | body | `string` | yes | The response format to return from Linkup search. Accepted values: `0`, `1`, `2`. |
| `maxResults` | body | `number` | no | Maximum number of results to return. |
| `includeImages` | body | `boolean` | no | Include image results in the response. |
| `fromDate` | body | `date` | no | Only consider results on or after this ISO date. |
| `toDate` | body | `date` | no | Only consider results on or before this ISO date. |
| `includeDomains[]` | body | `array<string>` | no | Restrict search results to these domains. |
| `excludeDomains[]` | body | `array<string>` | no | Exclude results from these domains. |
| `includeInlineCitations` | body | `boolean` | no | Include inline citations when the output type is sourcedAnswer. |
| `structuredOutputSchema` | body | `string` | no | A JSON schema string describing the structured output to return when output type is structured. |
| `includeSources` | body | `boolean` | no | Include source metadata when using structured output. |
