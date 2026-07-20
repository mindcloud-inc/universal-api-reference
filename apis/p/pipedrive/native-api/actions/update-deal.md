# Update Deal with Pipedrive

Updates an existing deal in Pipedrive.

## Endpoint

- **Method:** `PATCH`
- **Path:** `v2/deals/:id`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Update Deal](https://developers.pipedrive.com/docs/api/v1/Deals#updateDeal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency` | body | `string` | no | Currency code, e.g. USD. |
| `expected_close_date` | body | `string` | no | Expected close date (YYYY-MM-DD). |
| `id` | path | `number` | yes | Unique ID of the deal to update. |
| `lost_reason` | body | `string` | no | Lost reason text. |
| `status` | body | `string` | no | Deal status. |
| `title` | body | `string` | no | Deal title. |
| `owner_id` | body | `number` | no | Owner user ID. |
| `person_id` | body | `number` | no | Person ID linked to deal. |
| `org_id` | body | `number` | no | Organization ID linked to deal. |
| `pipeline_id` | body | `number` | no | Pipeline ID. |
| `stage_id` | body | `number` | no | Stage ID. |
| `value` | body | `number` | no | Deal value. |
| `probability` | body | `number` | no | Win probability percentage. |
