# Export keyword metrics with SE Ranking Data

Exports keyword metrics from SE Ranking Data.

## Endpoint

- **Method:** `POST`
- **Path:** `/keywords/export`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Export keyword metrics](https://seranking.com/api/data/keyword-research/#export)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cols` | body | `string` | no | Comma-separated fields to include in the export response. |
| `keywords` | body | `list<string>` | yes | List of keywords to export metrics for. |
| `sort` | body | `list<string>` | no | Optional sort field (for example: cpc). Accepted values: `competition`, `cpc`, `difficulty`, `volume`. |
| `sort_order` | body | `list<string>` | no | Optional sort order (asc or desc). Accepted values: `asc`, `desc`. |
| `source` | query | `string` | yes | Regional database code (for example: us). |
