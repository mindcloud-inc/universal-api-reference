# Search Signals By Summary Phrase with BuildBetter

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.buildbetter.app/v1`
- **Official documentation:** [Search Signals By Summary Phrase](https://docs.buildbetter.ai/pages/api/data-access#signals-extractions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchText` | body | `string` | yes | Filter signals whose summary matches this phrase. |
| `limit` | body | `number` | no | Maximum number of signals to return. |
