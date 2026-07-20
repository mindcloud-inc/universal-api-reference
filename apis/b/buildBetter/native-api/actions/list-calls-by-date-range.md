# List Calls by Date Range with BuildBetter

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.buildbetter.app/v1`
- **Official documentation:** [List Calls by Date Range](https://docs.buildbetter.ai/pages/api/graphql-queries#search-calls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | body | `string` | yes | Inclusive ISO timestamp for the start of the call window. |
| `dateTo` | body | `string` | yes | Inclusive ISO timestamp for the end of the call window. |
| `limit` | body | `number` | no | Maximum number of calls to return. |
