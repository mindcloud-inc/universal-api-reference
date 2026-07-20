# Get budget summary with Lunch Money

## Endpoint

- **Method:** `GET`
- **Path:** `/summary`
- **Base URL:** `https://api.lunchmoney.dev/v2`
- **Official documentation:** [Get budget summary](https://alpha.lunchmoney.dev/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | Inclusive start date (YYYY-MM-DD). |
| `end_date` | query | `string` | yes | Inclusive end date (YYYY-MM-DD). |
| `include_totals` | query | `boolean` | no | — |
| `include_occurrences` | query | `boolean` | no | — |
