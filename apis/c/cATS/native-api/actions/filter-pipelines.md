# Filter Pipelines with CATS

Finds pipelines in CATS by filter criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/pipelines/search`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Filter Pipelines](https://docs.catsone.com/api/v3/#pipelines-filter-pipelines)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `field` | body | `string` | yes | The field to filter on. |
| `filter` | body | `string` | yes | The filter operator to use. |
| `value` | body | `string` | yes | The value to filter by. |
