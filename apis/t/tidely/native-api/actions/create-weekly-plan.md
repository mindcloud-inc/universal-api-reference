# Create Weekly Plan with Tidely

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/open-api/plans`
- **Base URL:** `https://api.tidely.com`
- **Official documentation:** [Create Weekly Plan](https://api.tidely.com/tidely-open-api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `string` | no | Plan amount. |
| `date` | body | `string` | no | Plan date in YYYY-MM-DD format. |
| `name` | body | `string` | no | Name of the Tidely plan. |
| `type` | body | `string` | no | Plan type. Use ONE_TIME. |
