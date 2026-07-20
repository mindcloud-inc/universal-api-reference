# Extract Google AI Overview with Cloro

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/monitor/google`
- **Base URL:** `https://api.cloro.dev`
- **Official documentation:** [Extract Google AI Overview](https://docs.cloro.dev/api-reference/endpoint/google/ai-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | body | `string` | no | ISO 3166-1 alpha-2 country code for localized search results. |
| `query` | body | `string` | yes | The search query to execute on Google. |
| `include` | body | `object` | no | Optional flags for additional Google response data. |
| `include.aioverview` | body | `object` | no | Request Google AI Overview data in the Google Search response. |
| `include.aioverview.markdown` | body | `boolean` | no | Include markdown in the AI Overview response object. |
