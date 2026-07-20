# Filter Jobs with CATS

Finds jobs in CATS by filter criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/search`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Filter Jobs](https://docs.catsone.com/api/v3/#jobs-filter-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | The optional string to search within jobs for. |
| `field` | body | `string` | yes | The field to filter on. |
| `filter` | body | `string` | yes | The filter operator to use. |
| `value` | body | `string` | yes | The value to filter by. |
