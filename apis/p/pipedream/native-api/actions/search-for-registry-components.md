# Search for registry components with Pipedream

Finds registry components in Pipedream by natural-language query.

## Endpoint

- **Method:** `GET`
- **Path:** `/components/search`
- **Base URL:** `https://api.pipedream.com/v1`
- **Official documentation:** [Search for registry components](https://pipedream.com/docs/rest-api/api-reference/components/search-for-registry-components)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | query | `string` | no | Optional app name slug to filter results for a single app. |
| `debug` | query | `boolean` | no | Return additional debug data for result inspection when true. |
| `query` | query | `string` | yes | The natural-language query used to search the global registry. |
| `similarity_threshold` | query | `number` | no | Optional minimum similarity score between 0 and 1. |
