# Create Subindustry with Oboloo

Creates a new subindustry in Oboloo.

## Endpoint

- **Method:** `POST`
- **Path:** `/configuration/addsubIndustry`
- **Base URL:** `https://mindcloudwizard20260330.oboloo.app/api`
- **Official documentation:** [Create Subindustry](https://oboloo.app/api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `industries_id` | body | `string` | yes | Industry identifier that this subindustry belongs to. |
| `sub_industry_name` | body | `string` | yes | Name of the subindustry to create. |
