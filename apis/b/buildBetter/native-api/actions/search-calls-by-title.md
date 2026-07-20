# Search Calls By Title with BuildBetter

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.buildbetter.app/v1`
- **Official documentation:** [Search Calls By Title](https://docs.buildbetter.ai/pages/api/graphql-queries#search-calls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchText` | body | `string` | yes | Case-insensitive phrase to match against the call title. |
| `limit` | body | `number` | no | Maximum number of calls to return. |
