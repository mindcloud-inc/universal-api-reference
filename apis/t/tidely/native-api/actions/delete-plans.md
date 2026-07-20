# Delete Plans with Tidely

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/open-api/plans`
- **Base URL:** `https://api.tidely.com`
- **Official documentation:** [Delete Plans](https://api.tidely.com/tidely-open-api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryId` | query | `string` | no | Tidely category ID whose plans should be deleted. |
| `scenarioId` | query | `string` | no | Tidely scenario ID whose plans should be deleted. |
