# Create Research Task with LinkupAPI

Creates a new research task in LinkupAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/research`
- **Base URL:** `https://api.linkup.so/v1`
- **Official documentation:** [Create Research Task](https://docs.linkup.so/pages/documentation/api-reference/endpoint/post-research)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | body | `string` | yes | The natural-language research question to run. |
| `outputType` | body | `string` | yes | The research response format to request. Accepted values: `0`, `1`. |
| `maxResults` | body | `number` | no | Maximum number of results to use in the research task. |
| `includeImages` | body | `boolean` | no | Include image results in the research context. |
| `fromDate` | body | `date` | no | Only consider results on or after this ISO date. |
| `toDate` | body | `date` | no | Only consider results on or before this ISO date. |
| `includeDomains[]` | body | `array<string>` | no | Restrict research sources to these domains. |
| `excludeDomains[]` | body | `array<string>` | no | Exclude these domains from research sources. |
| `includeInlineCitations` | body | `boolean` | no | Include inline citations when the output type is sourcedAnswer. |
| `structuredOutputSchema` | body | `string` | no | A JSON schema string describing the structured output to return when output type is structured. |
| `includeSources` | body | `boolean` | no | Include source metadata when using structured output. |
