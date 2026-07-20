# Create Plan with Tidely

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/open-api/plans`
- **Base URL:** `https://api.tidely.com`
- **Official documentation:** [Create Plan](https://api.tidely.com/tidely-open-api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `string` | no | Plan amount. |
| `categoryId` | body | `string` | no | Tidely category ID. |
| `date` | body | `string` | no | Plan date in YYYY-MM-DD format. |
| `name` | body | `string` | no | Name of the Tidely plan. |
| `period` | body | `string` | no | Plan period: DAILY, WEEKLY, or MONTHLY. |
| `replaceCurrentValuesForThePeriod` | body | `string` | no | Whether to replace existing values for the same period. |
| `scenarioId` | body | `string` | no | Tidely scenario ID. |
| `type` | body | `string` | no | Plan type. Use ONE_TIME. |
